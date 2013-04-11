AOKP_Vigor
==========

Manifest for HTC Rezound needed for building AOKP

To initialize your local repository using the Vigor Device trees, use a command like this:

    repo init -u https://github.com/TheBr0ken/platform_manifest.git -b jb-mr1

Then to sync up:

    repo sync

Run this command to avoid breaking build:

    rm device/htc/vigor/overlay/packages/apps/Torch/res/values/config.xml

To Build:

    . build/envsetup.sh && brunch vigor
