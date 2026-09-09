# Android 14.0 LOS manifest for the Samsung p4note device family

### Init:

    repo init -u git://github.com/Viciouss/manifest_p4note.git -b lineage-21.0
    
### Status:

Don't use this if you have no idea what you are doing. There is unfinished stuff in here.

If you insist on using it, go ahead. Don't yell at me though, it's slow, has missing features,
and it might blow up in your face.

```bash
# if using CC (recommended)
export USE_CCACHE=1
ccache -M 50G

# preparing the build env
. build/envsetup.sh
# pick whatever device you have
lunch lineage_n8000-ap2a-userdebug
# this builds the project (use -jX with a lower number of cores if you are facing OOM, I build
# it with -j8 on a 32GB machine and it sometimes still crashes, just start it again)
m
# flashing via heimdall (don't forget to factory reset afterwards)
heimdall flash --SYSTEM out/target/product/n8000/system.img \
               --BOOT out/target/product/n8000/boot-debug.img \
               --HIDDEN out/target/product/n8000/vendor.img \
               --CACHE out/target/product/n8000/cache.img
```
