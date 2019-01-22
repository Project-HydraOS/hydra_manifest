HydraOS Project
===============

Download the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Initiate core trees without any device/kernel/vendor:

    repo init -u https://github.com/Project-HydraOS/hydra_manifest.git -b hydra-9.x

Then to sync up:

    repo sync -c -f -j8 --force-sync --no-clone-bundle --no-tags

*** 

Building 
-------- 

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on 
how to build.

    . build/envsetup.sh

    lunch You can also build for specific devices (eg. hydra) like this:

    . build/envsetup.sh
    lunch hydra_mido-userdebug
    mka hydra

Remember to `make clobber && make clean` every now and then!
