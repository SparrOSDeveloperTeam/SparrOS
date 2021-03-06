# SparrOS
The Official Release Site for SparrOS

## How to build

To build SparrOS, you will need to make sure that your linux (or cygwin) environment is set up to run buildroot. Then download [buildroot 2019.02.9 (LTS)](https://buildroot.org/downloads/buildroot-2019.02.9.tar.gz) and untar it. Download one of the following files:

* [SparrOS Config file for 32-bit machines (legacy boot)](https://raw.githubusercontent.com/SparrOSDeveloperTeam/sparros/master/config-sparros-x86)
* [SparrOS Config file for 64-bit machines (efi boot)](https://raw.githubusercontent.com/SparrOSDeveloperTeam/sparros/master/config-sparros-x64)
* [SparrOS Embedded Config file for Raspberry Pi 1/0 boards (ARMEL arm1176jzf*)](https://raw.githubusercontent.com/SparrOSDeveloperTeam/sparros-pi/master/config-sparros-embedded-armel)
* [SparrOS Embedded Config file for Raspberry Pi 3/4 boards (ARMHF cortex-a53)](https://raw.githubusercontent.com/SparrOSDeveloperTeam/sparros-pi/master/config-sparros-embedded-armhf)

Note: Raspberry Pi 2 boards were accidentally not supported in the alpha 0.0.1 build, oops. To correct this, set the Target Options for processors from cortex-a53 to cortex-a7.

Rename the downloaded config file to `.config` and place it in the root directory of the buildroot project (same directory as `Makefile`) and simply run

```
$ make
```

SparrOS x86/64 will build ISO files while SparrOS armel/armhf will build IMG files.
