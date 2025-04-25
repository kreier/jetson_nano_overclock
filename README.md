# jetson_nano_overclock

Kernel for nvidia jetson nano with some changes in dvfs for enable higher speed (2,0ghz+ and GPU 1,0ghz)

## Instructions to compile

1. Clone repository with `git clone https://github.com/kreier/jetson_nano_overclock`
2. `cd jetson_nano_overclock
3. execute `bash nvbuild.sh`
4. in kernel/kernel-4.9 execute `make && make install`
5. in `./kernel/kernel-4.9/arch/arm64/boot` you find the Image file you need to copy (probably with sudo) to `/boot/Image`, you can copy your existing one to another location beforehands so you have a backup to restore to
6. restart the nano

## Check status of CPU

- `jtop`
- `sudo jetson_clocks --show`

## Source

[https://forums.developer.nvidia.com/t/overclocking-jetson-nanos-cpu-and-gpu/83501/21](https://forums.developer.nvidia.com/t/overclocking-jetson-nanos-cpu-and-gpu/83501/21)
