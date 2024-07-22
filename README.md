SCFJS : Secure Comms For Journalistic Sources
WHISPRSCOOP
murmurnet

soc - test with beaglebone

1. login via web interface or tui
2. if device is untrsuted, (keystroke monitoring) create a keyboard interface to click
   with the mouse short messages (super unpractical, but allow to respond yes/no short messages)
   the keyboard interface could randomize key location as obfuscation each time it is loaded

3. Add 2FA

4. yubikey to access the secure web chat page
5. yubikey then on beaglebone to sign the messages (not encrypt them) allowing the recipient to verify if your are in danger or not
6. sd card to share long messages and files (pdf, images) in untrusted environment
7. zeroconf librairy (python\_ to advertise the device's IP address on LAN, then can access as beaglebone.local)
   6.b ip address scanning and display to user, using e-ink paper
8. Add option for bluetooth signature instead of yubikey
9. Show 2048 or candy crush game as the main thing to do on the yubikey as you either send large messages (from sd card)
   or let you check received messages and then read them in an off the air device
10. Device changes signature (mac, ip, etc) so that you have plausible deniability
11. send over TOR
12. add bluetooth for close-by communication

# Install

- avahi deamon - the beaglebone uses avahi to advertise its hostname on the local network.
  If the avahi deamon isn't running on your laptop, it won't work

```bash
systemctl status avahi-daemon
susdo systemctl start avahi-daemon
sudo pacman -S avahi
sudo systemlctl enable avahi-daemon
sudo systemctl start avahi-daemon
```

When connecting the bgbb via usb, it may create a separate network interface. Ensure that your device
is configure to route traffic correctly to the beaglebone.

The firewall might be blocking the necessary ports for avahi
If stopping the firewall resolves the issue, you may need to configure your firewall to allow avahi traffic

```bash
ip a
sudo systemctl stop firewalld
nmap -sn 192.168.7.0/24
```

# Packaging

wihin altoids mint metal boxes

# Features

- [ ] Virtual keyboard for clicks
- [ ] Check how to prevent screenshot and other likes
- [ ] Encapsulate traffic (check vasilik or bonfire)
- [ ] Duress function (press something, wrong password whatever to wipe all, including code)
- [ ] Game for being screpticious (2048 or candy crush)
- [ ] yubikey to sign messages (if held at gunpoint, the source would be able to allow the journalist to know the messages are not from him)
- [ ] Send messages from the sdcard (allowing to write/copy to an sdcard and then put into the secure drive to be shipped when connection is detected)
- [ ] Restrict device functionality based on geofencing

