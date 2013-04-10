AOKP_Vigor
==========

Manifest for HTC Rezound needed for building AOKP

To initialize your local repository using the Vigor Device trees, use a command like this:

    repo init -u https://github.com/TheBr0ken/platform_manifest.git -b jb-mr1

Then to sync up:

    repo sync

Run this command to avoid breaking build:

    rm device/htc/vigor/overlay/packages/apps/Torch/res/values/config.xml

Building ROM/Kernel with Linaro requires you to change 2 lines in build/envsetup.sh

Go into your "build" directory:

    cd build

edit envsetup.sh 

To build the ROM with linaro:

under

    ANDROID_EABI_TOOLCHAIN

change:

    arm) toolchaindir=arm/arm-linux-androideabi-4.6/bin

to:

    arm) toolchaindir=linaro/bin
    
To build the Kernel with linaro ( must use gcc/g++ 4.6 and up, kernel MUST have linaro support ):

under:

    ARM_EABI_TOOLCHAIN ARM_EABI_TOOLCHAIN_PATH
    
change:

    toolchaindir=arm/arm-eabi-4.6/bin

to:

    toolchaindir=linaro/bin
    

Build AOKP as normal


    

