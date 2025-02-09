# STM32MPU Buildroot external tree

This repository is a Buildroot `BR2_EXTERNAL` tree dedicated to
supporting the [STMicroelectronics](https://www.st.com)
[STM32MP1](https://www.st.com/en/microcontrollers-microprocessors/stm32mp1-series.html)
and [STM32MP2](https://www.st.com/en/microcontrollers-microprocessors/stm32mp2-series.html)
platforms. Using this project is not strictly necessary as Buildroot
itself has support for STM32MPU, but this `BR2_EXTERNAL` tree provide
example configurations demonstrating how to use the different features
of the STM32MPU platforms.

## Available configurations

This `BR2_EXTERNAL` tree provides height example Buildroot
configurations:

1. `st_stm32mp157d_dk1_defconfig`, which is a minimal configuration to
   support the [STM32MP157D Discovery Kit
   1](https://www.st.com/en/evaluation-tools/stm32mp157d-dk1.html)
   board. It builds the TF-A firmware, U-Boot bootloader, Linux kernel
   and a minimal user-space composed of just Busybox.

2. `st_stm32mp157d_dk1_demo_defconfig`, which is a more feature-ful
   configuration to support the [STM32MP157D-DK1 Discovery Kit
   1](https://www.st.com/en/evaluation-tools/stm32mp157d-dk1.html)
   board. It has support for OpenGL and Qt5 for graphics, for OP-TEE
   as a Trusted Execution Environment, for RAUC for OTA. It also shows
   how Device Tree files generated by CubeMX can be integrated in a
   Buildroot configuration.

3. `st_stm32mp157f_dk2_defconfig`, which is a minimal configuration to
   support the [STM32MP157F-DK2 Discovery Kit
   2](https://www.st.com/en/evaluation-tools/stm32mp157f-dk2.html)
   board. It builds the TF-A firmware, U-Boot bootloader, Linux kernel
   and a minimal user-space composed of just Busybox.

4. `st_stm32mp157f_dk2_demo_defconfig`, which is a more feature-ful
   configuration to support the [STM32MP157F-DK2 Discovery Kit
   2](https://www.st.com/en/evaluation-tools/stm32mp157f-dk2.html)
   board. It has support for OpenGL and Qt5 for graphics, for OP-TEE
   as a Trusted Execution Environment, for RAUC for OTA. It also shows
   how Device Tree files generated by CubeMX can be integrated in a
   Buildroot configuration.

5. `st_stm32mp135f_dk_defconfig`, which is a minimal configuration to
   support the [STM32MP135F Discovery Kit](https://www.st.com/en/evaluation-tools/stm32mp135f-dk.html)
   board. It builds the TF-A firmware, U-Boot bootloader, Linux kernel
   and a minimal user-space composed of just Busybox.

6. `st_stm32mp135f_dk_demo_defconfig`, which is a more feature-ful
   configuration to support the [STM32MP135F Discovery Kit](https://www.st.com/en/evaluation-tools/stm32mp135f-dk.html)
   board. It has support for OpenGL and Qt5 for graphics, for OP-TEE
   as a Trusted Execution Environment, for RAUC for OTA. It also shows
   how Device Tree files generated by CubeMX can be integrated in a
   Buildroot configuration.

7. `st_stm32mp257f_ev1_defconfig`, which is a minimal configuration to
   support the [STM32MP257F Evaluation board](https://www.st.com/en/evaluation-tools/stm32mp257f-ev1.html)
   board. It builds the TF-A firmware, U-Boot bootloader, Linux kernel
   and a minimal user-space composed of just Busybox.

8. `st_stm32mp257f_ev1_demo_defconfig`, which is a more feature-ful
   configuration to support the [STM32MP135F Evaluation board](https://www.st.com/en/evaluation-tools/stm32mp257f-ev1.html)
   board. It has support for Trusted-Firmware-m, for OpenGL and Qt5 for
   graphics, for OP-TEE as a Trusted Execution Environment, for RAUC for
   OTA. It also shows how Device Tree files generated by CubeMX can be
   integrated in a Buildroot configuration.

| Feature | st_stm32mp157d_dk1 | st_stm32mp157f_dk2 | st_stm32mp157d_dk1_demo | st_stm32mp157f_dk2_demo | st_stm32mp135f_dk | st_stm32mp135f_dk_demo | st_stm32mp257f_ev1 | st_stm32mp257f_ev1_demo |
| ------- | ------------------ | ------------------ | ----------------------- | ----------------------- | ----------------- | ---------------------- | ------------------ | ----------------------- |
| TF-A    | v2.8-stm32mp-r2 | v2.8-stm32mp-r2 | v2.8-stm32mp-r2 | v2.8-stm32mp-r2 | v2.8-stm32mp-r2 | v2.8-stm32mp-r2 | v2.8-stm32mp-r2 | v2.8-stm32mp-r2 |
| U-Boot  | v2022.10-stm32mp-r2 | v2022.10-stm32mp-r2 | v2022.10-stm32mp-r2 | v2022.10-stm32mp-r2 | v2022.10-stm32mp-r2 | v2022.10-stm32mp-r2 | v2022.10-stm32mp-r2 | v2022.10-stm32mp-r2 |
| Linux   | v6.1-stm32mp-r2 | v6.1-stm32mp-r2 | v6.1-stm32mp-r2 | v6.1-stm32mp-r2 | v6.1-stm32mp-r2 | v6.1-stm32mp-r2 | v6.1-stm32mp-r2 | v6.1-stm32mp-r2 |
| OP-TEE  | 3.19.0-stm32mp-r2 | 3.19.0-stm32mp-r2 | 3.19.0-stm32mp-r2 | 3.19.0-stm32mp-r2 | 3.19.0-stm32mp-r2 | 3.19.0-stm32mp-r2 | 3.19.0-stm32mp-r2 | 3.19.0-stm32mp-r2 |
| TF-M  | N/A | N/A | N/A | N/A | N/A | N/A | No | v1.7.0-stm32mp25-r9.1-w2425 |
| Qt5     | No | No | Yes | Yes | No | Yes | No | Yes |
| OpenGL  | No | No | Yes | Yes | No | Yes | No | Yes |
| WiFi    | N/A | No | N/A | Yes | No | Yes | N/A | N/A |
| Bluetooth | N/A | No | N/A | Yes | No | Yes | N/A | N/A |
| Audio    | No | No | Yes | Yes | N/A | N/A | N/A | N/A |
| Video    | N/A | N/A | N/A | N/A | No | Yes | No | Yes |
| CubeMX v6.12.0 Device Tree | No | No | Yes | Yes | No | Yes | No | No |
| Cortex M Firmware examples | No | No | Yes Cortex M4 | Yes Cortex M4 | N/A | N/A | No | Yes Cortex M33 |
| RAUC OTA | No | No | Yes | Yes | No | Yes | No | Yes |

Note that upstream Buildroot also contains pre-defined configurations
for STM32MPU platforms, but they use the upstream versions of TF-A,
U-Boot and Linux, while the configurations in this `BR2_EXTERNAL` tree
use the versions provided and supported by ST.

## Starter package

If you want to use Buildroot on STM32MPU platforms without building
everything yourself from source, we provide below a *Starter
Package*. For each release and each Buildroot configuration, we
provide:

* A README file that documents how the *Starter Package* has been
  built

* A pre-built image, ready to flash on an SD card, together with a
  *Block map* (which can be used with `bmaptool` to optimize the
  flashing process). This image contains a fully working system, with
  bootloaders, Linux kernel and root filesystem. Look at the [flash
  and boot section](#Flashing-and-booting-the-system) to discover how
  to use the prebuilt images.

* A Software Development Kit (SDK) that contains a cross-compiler and
  set of libraries that allow you to build applications for the
  target. See the Buildroot [advanced usage
  documentation](https://buildroot.org/downloads/manual/manual.html#_advanced_usage)
  to find out how to use the SDK.

* The complete list of open-source licenses and complete source code
  of all software components included in the pre-built image, for
  license compliance.

The following table provides the links to all these artifacts,
compiled with the latest
`openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26` release:

| Configuration | README | Image | Block map | SDK | Licences | Sources |
| ------------- | ------ | ----- | --------- | --- | -------- | ------- |
| st_stm32mp157d_dk1 | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp157d_dk1) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157d_dk1.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157d_dk1.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp157d_dk1.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp157d_dk1.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp157d_dk1.tar.gz) |
| st_stm32mp157d_dk1_demo | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp157d_dk1_demo) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157d_dk1_demo.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157d_dk1_demo.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp157d_dk1_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp157d_dk1_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp157d_dk1_demo.tar.gz) |
| st_stm32mp157f_dk2 | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp157f_dk2) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157f_dk2.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157f_dk2.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp157f_dk2.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp157f_dk2.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp157f_dk2.tar.gz) |
| st_stm32mp157f_dk2_demo | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp157f_dk2_demo) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157f_dk2_demo.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp157f_dk2_demo.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp157f_dk2_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp157f_dk2_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp157f_dk2_demo.tar.gz) |
| st_stm32mp135f_dk | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp135f_dk) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp135f_dk.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp135f_dk.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp135f_dk.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp135f_dk.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp135f_dk.tar.gz) |
| st_stm32mp135f_dk_demo | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp135f_dk_demo) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp135f_dk_demo.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp135f_dk_demo.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp135f_dk_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp135f_dk_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp135f_dk_demo.tar.gz) |
| st_stm32mp257f_ev1 | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp257f_ev1) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp257f_ev1.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp257f_ev1.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp257f_ev1.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp257f_ev1.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp257f_ev1.tar.gz) |
| st_stm32mp257f_ev1_demo | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/README-st_stm32mp257f_ev1_demo) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp257f_ev1_demo.img.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sdcard-st_stm32mp257f_ev1_demo.img.bmap) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/arm-buildroot-linux-gnueabihf_sdk-st_stm32mp257f_ev1_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/licenses-st_stm32mp257f_ev1_demo.tar.gz) | [URL](https://bootlin.com/pub/buildroot-st/openstlinux-6.1-buildroot-2024.02.3-mpu-v24.06.26/sources-st_stm32mp257f_ev1_demo.tar.gz) |

## Building Buildroot from source

### Pre-requisites

In order to use [Buildroot](https://www.buildroot.org), you need to
have a Linux distribution installed on your workstation. Any
reasonably recent Linux distribution (Ubuntu, Debian, Fedora, Redhat,
OpenSuse, etc.) will work fine.

Then, you need to install a small set of packages, as described in the
[Buildroot manual System requirements
section](https://buildroot.org/downloads/manual/manual.html#requirement).

For Debian/Ubuntu distributions, the following command allows to
install the necessary packages:

```bash
$ sudo apt install debianutils sed make binutils build-essential gcc g++ bash patch gzip bzip2 perl tar cpio unzip rsync file bc git
```

There are also optional dependencies if you want to use Buildroot features
like interface configuration, legal information or documentation.
Please see the [corresponding manual section](https://buildroot.org/downloads/manual/manual.html#requirement-optional).

### Getting the code

This `BR2_EXTERNAL` tree is designed to work with the `2024.02.x` LTS
version of Buildroot. However, we needed a few changes on top of
upstream Buildroot, so you need to use our own Buildroot fork together
with this `BR2_EXTERNAL` tree, and more precisely its `st/2024.02.3`
branch.

```bash
$ git clone -b st/2024.02.3 https://github.com/bootlin/buildroot.git
```

See our documentation on [internal details](docs/internals.md) for more
information about the changes we have compared to upstream Buildroot.

Now, clone the matching branch of the `BR2_EXTERNAL` tree:

```bash
$ git clone -b st/2024.02.3 https://github.com/bootlin/buildroot-external-st.git
```

You now have side-by-side a `buildroot` directory and a
`buildroot-external-st` directory.

### Configure and build

Go to the Buildroot directory:

```bash
$ cd buildroot/
```

And then, configure the system you want to build by using one of the 8
*defconfigs* provided in this `BR2_EXTERNAL` tree. For example:

```bash
buildroot/ $ make BR2_EXTERNAL=../buildroot-external-st st_stm32mp157f_dk2_defconfig
```

We are passing two informations to `make`:

1. The path to `BR2_EXTERNAL` tree, which we have cloned side-by-side
to the Buildroot repository

2. The name of the Buildroot configuration we want to build.

If you want to further customize the Buildroot configuration, you can
now run `make menuconfig`, but for your first build, we recommend you
to keep the configuration unchanged so that you can verify that
everything is working for you.

Start the build:

```bash
buildroot/ $ make
```

This will automaticaly download and build the entire Linux system for
your STM32MPU platform: cross-compilation toolchain, firmware,
bootloader, Linux kernel, root filesystem. It might take between 30
and 60 minutes depending on the configuration you have chosen and how
powerful your machine is.

## Flashing and booting the system

The Buildroot configurations generate a compressed ready-to-use SD card
image, available as `output/images/sdcard.img.gz`. You can also use the
prebuilt images downloaded from the [starter package section](#Starter-package).

Flash this image on a SD card:

```bash
buildroot/ $ gzip -dc sdcard.img.gz | dd of=/dev/sdX bs=1M
```

You can also use the block map image file to accelerate the flashing
process. The block map image is available as
`output/images/sdcard.img.bmap` or can be downloaded from the
[starter package section](#Starter-package). Both the block map file and
the SD card image has to be in the same directory.

Note: bmaptool will not erase empty partition like the U-boot environment
partition.

```bash
buildroot/ $ bmaptool copy sdcard.img.gz /dev/sdbX
```

(Note: this assumes your SD card appears as `/dev/sdX` on your system.)

Then:

1. Insert the microSD card
   - STM32MP157: connector CN15
   - STM32MP135: connector CN3
   - STM32MP257: connector CN1

2. Plug a micro-USB cable or USB-C for STM32MP257 and run your serial
communication program on /dev/ttyACM0.
   - STM32MP157: connector CN11
   - STM32MP135: connector CN10
   - STM32MP257: connector CN21

3. Configure the SW1 switch to boot on SD card
   - STM32MP157: BOOT0 and BOOT2 to ON
   - STM32MP135: BOOT0 to ON, BOOT1 to OPEN, BOOT2 to ON
   - STM32MP257: BOOT0 to ON, BOOT1 and BOOT2 and BOOT3 to OPEN

4. Plug a USB-C cable or Barrel cable for STM32MP257 to power-up the board
   - STM32MP157: connector CN6
   - STM32MP135: connector CN12
   - STM32MP257: connector CN20

5. The system will start, with the console on UART. You can log-in as
`root` with no password for the minimal configuration, or with `root`
as the password for the demo configurations.

Note: it is also possible to flash the SD card while leaving it into
the board, by using the STM32 Cube Programmer. See our [Using the
STM32 Cube Programmer](docs/stm32cubeprogrammer.md) page for more
details.

# Going further

* [Using the STM32 Cube Programmer](docs/stm32cubeprogrammer.md)
* [Using Device Tree files generated by STM32 CubeMX](docs/stm32cubemx.md)
* [Using the Firmware examples for the Cortex M](docs/cortexm.md)
* [Testing display support](docs/display.md)
* [Using WiFi](docs/wifi.md)
* [Using Bluetooth](docs/bluetooth.md)
* [Using Audio](docs/audio.md)
* [Using Camera](docs/camera.md)
* [Using Qt5 demos](docs/qt5.md)
* [Using OP-TEE](docs/optee.md)
* [Using OTA with RAUC](docs/ota.md)
* [Internal details](docs/internals.md) on this `BR2_EXTERNAL` tree
* [Release notes](docs/release-notes.md)

# References

* [Buildroot](https://buildroot.org/)
* [Buildroot reference manual](https://buildroot.org/downloads/manual/manual.html)
* [Buildroot system development training
  course](https://bootlin.com/training/buildroot/), with freely
  available training materials

# Support

You can contact Bootlin at info@bootlin.com for commercial support on
using Buildroot on STM32MP1 and STM32MP2 platforms.
