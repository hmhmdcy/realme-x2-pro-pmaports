# Realme X2 Pro / samurai userspace adaptation

This is the public userspace/package fork for the Realme X2 Pro
(RMX1931 / RMX1931CN, codename `samurai`).  It is a personal
postmarketOS/Nura adaptation fork, not official upstream device support.

## Public entry points

- System releases (boot/kernel/DTB/recovery):
  https://github.com/hmhmdcy/realme-x2-pro-releases
- Signed userspace APK repository:
  https://github.com/hmhmdcy/realme-x2-pro-apk
- Kernel source:
  https://github.com/hmhmdcy/realme-x2-pro-linux
- Integration/docs/patches:
  https://github.com/hmhmdcy/realme-x2-pro-edk2

## Branches

The public default branch is `stable`, based on the earlier
`codex/standard-arm64-settings` snapshot.  Development and historical
branches are not consumer release channels.

Package recipes live under `device/testing/` for now.  A package being
present here does not mean it is accepted into the official pmaports
testing/community repository.

## Current package baseline

The published APK repository is the authority for tested package
versions and hashes.  The system release manifest is the authority for
the kernel/boot/DTB combination.  Do not mix package updates with a
kernel or boot change in the same window.

## Reproducibility and limits

- The device package currently uses an external `kernel-none` subpackage;
  the kernel is not installed by `apk`.
- The 8 GiB unit is the current test unit.  6/12 GiB and
  64/128/256 GB SKUs are not all validated.
- Do not distribute vendor firmware, calibration, NV, persist or
  userdata.
- For clean-image, migration and recovery rules see the releases
  repository.