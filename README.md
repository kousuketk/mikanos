# mikanos

### setup
```
- edk2
$ ln -s /workspaces/mikanos/MikanLoaderPkg ./
$ source edksetup.sh
- Conf/target.txtを編集
ACTIVE_PLATFORM:MikanLoaderPkg/MikanLoaderPkg.dsc
TARGET:DEBUG
TARGET_ARCH:X64
TOOL_CHAIN_TAG:CLANG38
```

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

### Note
- qumeに不具合があるときは、dockerから再build```
