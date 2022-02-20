# AMI OpenBMC build for OCP Tioga Pass

These are instructions on how to build the AMI OpenBMC build for the OCP Tioga Pass Platform. It's important that you sync the versions of the OpenBMC with the AMI BIOS image.

## Set up the build environment.

Included is a vagrantfile that you can use to build a VM to do your build. I would reserve about 150G of space to do the build. Depending how much parallelism you want, you should set the memory and number of cores accordingly.

``` sudo apt-get install -y git build-essential libsdl1.2-dev texinfo gawk chrpath diffstat ```

``` sudo apt-get install build-essential git make -y ```

``` sudo apt-get update ```

``` sudo apt-get install -y python3 python-git python-yaml ```


``` mkdir -p ~/build ```

```  git clone https://github.com/opencomputeproject/MegaRAC-OpenEdition openbmc ```

``` cd openbmc ```

``` $ . setup ```

``` TEMPLATECONF=meta-ami/meta-tiogapass/conf  . openbmc-env ```

``` bitbake obmc-phosphor-image ```

The resultant image will be located in ~/build/openbmc/build/tmp/deploy/images/tiogapass/obmc-phosphor-image-tiogapass.static.mtd and whatever it is symlinked to.
