# TWRP 10 for Moto E7 Plus

### How to build ###

```bash
# Create dirs
$ mkdir tw; cd tw

# Init repo
$ repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-10.0

# Clone guam repo
$ git clone https://github.com/yukosky/android_device_motorola_guam -b twrp-10.0 device/motorola/guam

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ source build/envsetup.sh; lunch omni_guam-eng; mka recoveryimage
```

## Credits
* betaxab/contributors: For ```ginna``` device tree base