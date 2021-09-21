### run
```
- kernel.elfを作る
$ cd kernel
$ clang++ $CPPFLAGS -O2 --target=x86_64-elf -fno-exceptions -ffreestanding -c main.cpp
$ ld.lld $LDFLAGS --entry KernelMain -z norelro --image-base 0x100000 --static -o kernel.elf main.o
- buildして実行
$ cd ~/edk2
$ source edksetup.sh
$ build
$ ~/osbook/devenv/run_qemu.sh ~/edk2/Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi /workspaces/mikanos/kernel/kernel.elf
```