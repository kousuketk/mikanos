### run
```
- kernel.elfを作る
$ cd kernel
$ source $HOME/osbook/devenv/buildenv.sh
$ make
- buildして実行
$ cd ~/edk2
$ source edksetup.sh
$ build
$ ~/osbook/devenv/run_qemu.sh ~/edk2/Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi /workspaces/mikanos/kernel/kernel.elf
```