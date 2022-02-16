# Yosemite v1 OCP Mono Lake OpenBMC Build instructions

These are the build instructions on how to build the FB openbmc image
for the Yosemite v1 Mono Lake OCP Platform.

Pre-requisites:
You will need to have an Ubuntu 18.04 image. Included in the repo is a
Vagrant image that can be used to build a build VM with all the pre-requisites. Any contributions to make such build images streamlined would be appreciated!

After building your VM:

Setup the build environment.
``` $ sudo apt-get update && sudo apt-get install -yy gawk wget git-core
diffstat unzip texinfo gcc-multilib build-essential chrpath socat cpio
python python3 python3-pip python3-pexpect xz-utils debianutils
iputils-ping ```

``` $ sudo apt-get update && sudo apt-get install -yy gawk wget git-core
diffstat unzip texinfo gcc-multilib build-essential chrpath socat cpio
python python3 python3-pip python3-pexpect xz-utils debianutils
iputils-ping ```

``` $ sudo apt-get install ca-certificates
    $ sudo apt-get update
    $  sudo apt-get dist-upgrade
    $  sudo apt-get install apt-transport-https ca-certificates -y
```
