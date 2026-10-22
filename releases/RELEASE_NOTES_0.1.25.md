# Android 2.80 / TV firmware 0.1.25

Release pairing: Android versionCode 64, TV ARMv6 protocol 1.

TV Wi-Fi now uses one persistent password shared through authenticated encrypted Bluetooth setup. Returning phones can join the existing hotspot without rotating its password. Includes authenticated race-session handover, bounded setup and Bluetooth recovery, snapshot traffic rate limiting, and clearer connection guidance. Each phone needs app 2.80 and one setup connection to learn the shared password. Install the APK over the existing app; do not uninstall.

Validation: 88 Android unit tests, Android lint, and 90 TV tests passed. Seeded tests include 1,000 shared-password provisions across four simulated phones, plus handover, persistence, authorization, and failure recovery. Signed firmware integrity and invalid-signature rejection verified.

Physical acceptance: user reports many consecutive fast S21/S26 handovers after migration. One S26 report measured 8.292 seconds using only the saved-network join and display connection. One intermittent S21 connection failure remains unresolved; this release does not claim failure-free connections. Earlier unexpected Pi reboot/kernel-fault investigation also remains open. Persistent diagnostic logging was enabled on the test Pi separately; it is not installed by this application release.

Known limitations: initial per-phone migration can use the slower full Bluetooth/hotspot path. Older apps cannot replace an established shared password with a different password. Only one phone controls the display at a time. Repeat a failed connection and retain the diagnostic timing report if it recurs.
