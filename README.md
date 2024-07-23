# SCFJS: Secure Comms For Journalistic Sources

> **Note:** This is a work in progress project.

> **Project brief:**
> Software to run on  an embedded linux device allowing ones to exchange information is anonymously as possible in untrusted/heavily monitored environments

## Project Names

- **WHISPRSCOOP**
- **murmurnet**

## Packaging

- BeagleBone
  - wihin altoids mint metal boxes
- [USB armory Mk II](https://github.com/usbarmory/usbarmory/wiki/Mk-II-Introduction)
  - As is, usb key

## Features

- [ ] **Virtual keyboard** to click in untrusted environments (cybercafe, suspicion of keystroke monitoring). Randomize key locations as obfuscation each time it is loaded
- [ ] **Login** via WebUI or TUI
- [ ] **2FA**
  - Message signing, allowing the recipient to verify if correspondent is in danger or not
  - Secure access (Login to webpage, otherwise show usb content documents or game page)
- [ ] **SD Card support** To send long messages/documents in an untrusted environment (i.e. automated)
- [ ] **mDNS** Use zeroconf to advertise the device's IP on LAN, then access it as "mydevice.local"
- [ ] **Bluetooth Signature Option**
  - Add an option for Bluetooth signature instead of YubiKey.
- [ ] **Disguise Feature**
  - Show 2048 or Candy Crush game as the main activity to disguise the true purpose of the device.
- [ ] **Plausible Deniability**
  - Device changes signature (MAC, IP, etc.) for plausible deniability.
- [ ] **TOR Integration**
  - Send messages over TOR (already a Simplex-Chat feature).
