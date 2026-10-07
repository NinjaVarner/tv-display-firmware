# TV firmware 0.1.6 / Android 2.11

- Temporary TV debug panel shows Wi-Fi/IP, connection progress, and persistent error codes; `NINJA_DISPLAY_DEBUG=0` hides it.
- Bluetooth setup remains available without a five-minute deadline and releases the setup connection when the phone disconnects.
- Bluetooth diagnostics, Wi-Fi reset/change, and reboot controls preserve phone registration; recovery actions are blocked during a known active race or update.
- Android setup centers the dark gray/royal blue refresh button and aligns network choices left. Selecting a secured network focuses and reveals the password above the keyboard.
- TV UI adds larger headings, optional IP entry, selectable text, concise instructions, and correct connected/disconnected button states.
- Buzzer UI adds remembered editable names and compact battery voltage/percentage; battery telemetry requires buzzer firmware 1.4.0 and an onboard MAX17048 or LC709203F gauge.

Validation: TV Python suite, native ARMv6 renderer build/test and screenshot, Android unit tests and emulator Wi-Fi/password tests, and buzzer PlatformIO build/image verification. Physical BLE/Wi-Fi recovery, battery readings and OTA activation remain to be checked on the devices.

# Firmware 0.1.5

Bluetooth setup, phone enrollment and Wi-Fi recovery start automatically from the app. Compare the pairing code on the TV and phone and confirm Android's system prompt. No TV button is required.

Setup sessions last five minutes and belong to one phone. Authenticated BLE encryption remains required. Existing phone credentials and Wi-Fi profiles are preserved. The native TV prompt now directs users to the app.

The corrected manual patch was confirmed working on the Pi. Automated tests, native ARMv6 renderer tests, package signature verification and invalid-signature rejection passed. Installation through Android remains a hardware acceptance check.
