# Firmware 0.1.5

Bluetooth setup, phone enrollment and Wi-Fi recovery start automatically from the app. Compare the pairing code on the TV and phone and confirm Android's system prompt. No TV button is required.

Setup sessions last five minutes and belong to one phone. Authenticated BLE encryption remains required. Existing phone credentials and Wi-Fi profiles are preserved. The native TV prompt now directs users to the app.

The corrected manual patch was confirmed working on the Pi. Automated tests, native ARMv6 renderer tests, package signature verification and invalid-signature rejection passed. Installation through Android remains a hardware acceptance check.
