# A2DP_BlueetothMacddress-ESP
ESP32 Bluetooth Audio Streaming

Overview

This project utilizes the ESP32 and the ESP32-A2DP library to stream high-quality audio via the Bluetooth A2DP protocol to a True Wireless Stereo (TWS) device. The system locks onto a specific device's MAC address to ensure a stable and uninterrupted connection, preventing random device pairings.

Features

Bluetooth A2DP streaming: High-quality audio transmission to TWS devices.
SD card audio playback: Select and play audio files stored on an SD card.
MAC address locking: Ensures connection stability by pairing only with a designated TWS device.
Playback control: Start, pause, stop, and switch tracks via user input.
Optimized Bluetooth scanning: Prevents excessive rescanning and MAC address duplication.
EEPROM storage: Saves the target MAC address to avoid repetitive scanning.

Hardware Requirements

ESP32 development board
MicroSD card module (for audio storage)
TWS Bluetooth speaker/headphones
Power supply (USB or battery)
Software Requirements

Library
1. https://github.com/earlephilhower/ESP8266Audio
2. https://github.com/pschatzmann/ESP32-A2DP
3. https://github.com/pschatzmann/arduino-audio-tools

Installation & Setup

Install dependencies

Install the ESP32 board package in Arduino IDE.
Add the ESP32-A2DP library via Library Manager.
Ensure SD and EEPROM libraries are included.
Prepare the SD card
Format the SD card as FAT32.
Copy WAV or MP3 files to the root directory.
Upload the code
Open the Arduino project.
Modify the MAC address handling logic if needed.
Compile and upload the code to the ESP32.
Connect to the TWS device
The ESP32 will scan and connect to the saved MAC address.
If no MAC is stored, it will prompt the user to select a device.

Usage

Initial pairing: Scan for Bluetooth devices and select a TWS device.
Audio playback: Play stored audio files from the SD card.

Control options:

Play/Pause: Control playback state.
Next/Previous Track: Switch between files.
Reconnect: Rescan and connect if needed.

Code Structure

main.ino: Handles setup, initialization, and main loop.

bluetooth.ino: Manages Bluetooth scanning, pairing, and connection.

audio.ino: Handles SD card reading and audio streaming.

storage.ino: Saves and retrieves MAC addresses from EEPROM.

Debugging & Troubleshooting

Common Issues & Solutions

Issue

Possible Cause

Solution

ESP32 not detecting TWS

Bluetooth scanning issue

Restart the ESP32 and ensure the TWS device is in pairing mode

Audio playback stutters

Weak Bluetooth signal

Reduce interference, keep ESP32 close to the TWS device

MAC address not saving

EEPROM write failure

Check EEPROM write logic and increase write delay if necessary

SD card not detected

Incorrect wiring or format

Ensure proper wiring and format SD card to FAT32

License

This project is open-source under the MIT License.

Acknowledgments

Special thanks to the ESP32-A2DP library developers for enabling Bluetooth audio streaming on ESP32.

Contributions & Feedback

Feel free to open an issue or submit a pull request if you find bugs or have improvements to suggest!

