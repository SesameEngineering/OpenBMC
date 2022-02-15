These contain the assets to build the OpenBMC image for Tioga Pass.

To successfully build the Tioga Pass image, you should build a vagrant
machine that builds Ubuntu 16.04. Make sure you have approximately 75GB of
space reserved for the build.

Once you've spun up the VM. Prepare your build environment. Please refer to
the notes on
[pre-requisites](https://www.yoctoproject.org/docs/2.5/brief-yoctoprojectqs/brief-yoctoprojectqs.html).

```sh
sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib      build-essential chrpath socat cpio python python3 python3-pip python3-pexpect      xz-utils debianutils iputils-ping libsdl1.2-dev xterm -y
sudo apt-get install ca-certificates mac-util -y
sudo apt-get install -y git tar python3 -y
sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib      build-essential chrpath socat cpio python python3 python3-pip python3-pexpect      xz-utils debianutils iputils-ping -y

sudo apt-get install python-git -y
sudo apt-get install ninja -y
sudo apt-get install python3-pyflakes
```

To get started with the build:

```sh
$ git clone -b helium https://github.com/facebook/openbmc.git
$ cd openbmc
$ ./sync_yocto.sh
```

```sh
$ source openbmc-init-build-env source openbmc-init-build-env fbtp
```

```
$ bitbake bitbake fbtp-image
```

The resultant image should be located in
build/openbmc/build/tmp/deploy/images/fbtp as flash-fbtp (or the image that
it is symlinked to)

There is more documentation in how to flash in the wiki.
