# Ninja TV Display firmware

Signed firmware packages and the update catalog used by CourseTimer Android 2.10 and newer.

On your phone, connect to the TV, finish the current race, open Connect TV Display, and choose Check GitHub for TV updates, then Download and install. Android 2.10 also includes firmware 0.1.5 for offline installation. You do not need to download a ZIP manually.

The app checks compatibility, package size and SHA-256. The TV verifies the Ed25519 signature and payload hashes before installing. Updates preserve saved Wi-Fi and enrolled phone credentials.

- [Update catalog](tv-firmware.json)
- [Firmware 0.1.5](releases/ninja-display-0.1.5.zip)
- [SHA-256 checksum](releases/ninja-display-0.1.5.zip.sha256)
- [Release notes](RELEASE_NOTES.md)
- [Public verification key](update-ed25519.pub)

The public key is for verification only. For first-time key installation, verify its fingerprint through your trusted commissioning process. This repository contains no private signing keys or device credentials. Application source repositories remain private.

Firmware ZIPs are signed application updates for an existing Raspberry Pi Zero W display installation. They are not SD card images or buzzer firmware.
