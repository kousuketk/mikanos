# mikanos

### overview
![image](https://user-images.githubusercontent.com/42241308/137346787-0cf71915-1adb-4635-8886-75f6291cd084.png)


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
$ APPS_DIR=apps RESOURCE_DIR=resource ./build.sh run
```

### Note
- qumeに不具合があるときは、dockerから再build
- VSCodeの"Reopen in Container"で、docker内のファイルとlocalのファイルを同期
