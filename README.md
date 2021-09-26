# mikanos

### setup
```
- kernel
$ cd kernel
$ source $HOME/osbook/devenv/buildenv.sh
- edk2
$ cd ~/edk2
$ ln -s /workspaces/mikanos/MikanLoaderPkg ./
$ source edksetup.sh
- Conf/target.txtを編集
ACTIVE_PLATFORM:MikanLoaderPkg/MikanLoaderPkg.dsc
TARGET:DEBUG
TARGET_ARCH:X64
TOOL_CHAIN_TAG:CLANG38
$ build
- XQuartz
$ xhost + 127.0.0.1
```

### run
```
- kernel
$ cd kernel
$ make
- edk2
$ cd ~/edk2
$ ~/osbook/devenv/run_qemu.sh ~/edk2/Build/MikanLoaderX64/DEBUG_CLANG38/X64/Loader.efi /workspaces/mikanos/kernel/kernel.elf
```

### Note
- qumeに不具合があるときは、dockerから再build
- VSCodeの"Reopen in Container"で、docker内のファイルとlocalのファイルを同期
