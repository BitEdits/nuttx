# Synrc RTS

Synrc RTS is a specialized distribution of Apache NuttX RTOS
tailored for needs of Synrc Skynet application,
supporting a curated set of hardware platforms.

Synrc RTS is a lightweight fork of NuttX, optimized
to support specific boards for real-time applications.
It retains the core functionality of NuttX
while focusing on the following platforms:

* SIM: POSIX-based simulation environment
* QEMU: ARMv7-A virtualization
* Sony Spresense: CXD5602
* Raspberry Pi Pico: RP2040
* Raspberry Pi Pico 2: RP2350
* PinePhone Pro: RK3399

## QEMU Virual Board

If you don't have 32-bit ARM-v7 board yet, then you can try QEMU.

```
./tools/configure.sh qemu-armv7a:nsh
make menuconfig
make
qemu-system-arm -M virt -device loader,file=nuttx -nographic
```

## SIM POSIX Executable

```
./tools/configure.sh sim:nsh
make menuconfig
make
./nuttx
```

## Pico 2 Firmware

```
./tools/configure.sh raspberrypi-pico-2:usbnsh
make menuconfig
make
```

## License

Synrc RTS is licensed under the Apache License 2.0.
It is a derivative of Apache NuttX,
modified to support the listed boards.
See the NOTICE file for details.

## Acknowledgment

Based on <a href="https://nuttx.apache.org/">Apache NuttX RTOS</a>.
Thanks to Gregory Nutt and the NuttX community for their foundational work.

## Author

* Namdak Tonpa
