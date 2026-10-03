# TWRP manifest for the Samsung p4note device family

### Init:

    repo init -u ssh://git@github.com/Viciouss/manifest_p4note.git -b twrp-9_nougat

### Build:

    . build/envsetup.sh
    export ALLOW_MISSING_DEPENDENCIES=true
    export LC_ALL=C
    lunch omni_p4note-userdebug
    mka recoveryimage


### Status:

Don't use this if you have no idea what you are doing. There is unfinished stuff in here.
