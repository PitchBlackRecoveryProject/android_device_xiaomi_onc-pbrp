The Xiaomi Redmi 7/Y3 (codenamed _"onc"_) is a mid-range smartphone from Xiaomi.
It was announced on March, 2019.

Basic | Spec Sheet
-------:|:-------------------------
SoC | Qualcomm MSM8953 Snapdragon 632
CPU | Octa core (1.8 GHz, Quad core, Kryo 250 + 1.8 GHz Quad core, Kryo 250)
GPU | Adreno 506
Shipped Android Version | Android 9.0 with MIUI 10

## Device picture

![Xiaomi Redmi 7/Y3](https://i.imgur.com/PjaQrqr.png "Xiaomi Redmi 7/Y3")

## Features

Works:
* ADB
* Decryption of /data
* Screen brightness settings
* MTP
* Flashing
* Backup/Restore
* USB OTG
* Vibration

## Sync and Build manually
---------------

To get started with building PitchBlack Recovery, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

To initialize your local repository using the minimal-manifest-twrp omni trees to build PitchBlack Recovery, use a command like this:

```bash
repo init --depth=1 -u https://github.com/PitchBlackRecoveryProject/manifest_pb.git -b android-9.0
repo sync -j$(nproc --all) --force-sync
```

## Add these projects to .repo/manifests/twrp-extras.xml
```xml
<project path="TheSync/pbrp" remote="github" revision="android-9.0" />
```

## Then to build
```bash
     cd <source-dir>
     . build/envsetup.sh
     lunch omni_onc-eng && mka recoveryimage
```

## To test it
```
fastboot flash recovery out/target/product/onc/recovery.img
```

## Kernel source
```
https://github.com/TheSync/android_kernel_xiaomi_onclite/tree/recovery
```
