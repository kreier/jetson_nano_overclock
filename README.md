# jetson_nano_overclock

Kernel for nvidia jetson nano with some changes in dvfs for enable higher speed (2,0ghz+ and GPU 1,0ghz)

## Instructions to compile

1. Clone repository with `git clone https://github.com/kreier/jetson_nano_overclock`
2. `cd jetson_nano_overclock
3. execute `bash nvbuild.sh` - this will take some hours on the Jetson Nano
4. in kernel/kernel-4.9 execute `make && make install`
5. in `./kernel/kernel-4.9/arch/arm64/boot` you find the Image file you need to copy (probably with sudo) to `/boot/Image`, you can copy your existing one to another location beforehands so you have a backup to restore to
6. restart the nano

## Check status of CPU

- `jtop`
- `sudo jetson_clocks --show`

## Source

- [https://forums.developer.nvidia.com/t/overclocking-jetson-nanos-cpu-and-gpu/83501/21](https://forums.developer.nvidia.com/t/overclocking-jetson-nanos-cpu-and-gpu/83501/21)
- [https://docs.nvidia.com/jetson NVIDIA Jetson Linux Developer Guide 32.7.5 - Power Management for Jetson Nano and Jetson TX1 Devices](https://docs.nvidia.com/jetson/archives/l4t-archived/l4t-3275/index.html#page/Tegra%20Linux%20Driver%20Package%20Development%20Guide/power_management_nano.html)
- 32.7.5 is the oldest in the archive, April 2025 the current version is 36.4.3 with Jetpack 6.2 (instead of 4.6.6) [https://docs.nvidia.com/jetson/archives/](https://docs.nvidia.com/jetson/archives/)
