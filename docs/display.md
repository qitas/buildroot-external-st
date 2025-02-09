# Testing display support

Applicable platforms: STM32MP257F-EV1, STM32MP157-DK1, STM32MP157-DK2, STM32MP135-DK

The different platforms have the following capabilities:
* STM32MP157-DK1: HDMI output
* STM32MP157-DK2: DSI display panel and HDMI output
* STM32MP135-DK: DSI display panel
* STM32MP257-EV1: LVDS display panel

The *demo* configurations for all platforms include the `modetest`
utility, which allows low-level testing of display devices, directly
by using *DRM* devices.

First you can run `modetest -c` to enumerate the connectors available
on your system. On the STM32MP157-DK2, the output looks like this:

```
# modetest -c
...
trying to open device 'stm'...done
Connectors:
id      encoder status          name            size (mm)       modes   encoders
32      0       connected       HDMI-A-1        480x270         5       31
  modes:
        index name refresh (Hz) hdisp hss hse htot vdisp vss vse vtot
  #0 1280x720 60.00 1280 1390 1430 1650 720 725 730 750 74250 flags: phsync, pvsync; type: driver
  #1 1280x720 50.00 1280 1720 1760 1980 720 725 730 750 74250 flags: phsync, pvsync; type: driver
  #2 800x600 75.00 800 816 896 1056 600 601 604 625 49500 flags: phsync, pvsync; type: driver
  #3 720x576 50.00 720 732 796 864 576 581 586 625 27000 flags: nhsync, nvsync; type: driver
  #4 720x480 59.94 720 736 798 858 480 489 495 525 27000 flags: nhsync, nvsync; type: driver
...
34      0       connected       DSI-1           52x86           1       33
  modes:
        index name refresh (Hz) hdisp hss hse htot vdisp vss vse vtot
  #0 480x800 50.00 480 578 610 708 800 815 825 839 29700 flags: ; type: preferred, driver
```

So we can see that we have two connectors: connector `32` is the HDMI
output, while connector `34` is the DSI panel. Obviously, the results
on other platforms will be different.

## STM32MP157-DK1

You can test the HDMI output by displaying `modetest` default picture,
for example in a 720p resolution:

```
# modetest -M stm -s 32:1280x720
```

## STM32MP157-DK2

You can test the HDMI output by displaying `modetest` default picture,
for example in a 720p resolution:

```
# modetest -M stm -s 32:1280x720
```

You can test the DSI display panel by displaying the `modetest`
default picture, in the native DSI panel resolution:

```
# modetest -M stm -s 34:480x800
```

You can change the DSI display panel backlight value from 0 to
`max_brightness`:

```
# cat /sys/class/backlight/5a000000.dsi.0/max_brightness
255
# echo 10 > /sys/class/backlight/5a000000.dsi.0/brightness
```

## STM32MP135-DK

You can test the DSI display panel by first enabling the display
backlight:

```
# echo 1 >  $(realpath /sys/class/backlight/panel-*)/brightness
```

And then displaying the `modetest` default picture, in the default DSI
panel resolution:

```
# modetest -M stm -s 32:#0
```

## STM32MP257-EV1

You can test the LVDS output by displaying `modetest` default picture,
in the default resolution:

```
# echo 1 >  $(realpath /sys/class/backlight/panel-*)/brightness
# modetest -M stm -s 32:#0
```
