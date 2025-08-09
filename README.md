# My-personal-linux-setup
This is inspired by this project which is for fedora but I've made this for small general tweaks: https://github.com/wz790/Fedora-Noble-Setup
1. Make boot times faster: ```sudo systemctl disable NetworkManager-wait-online.service```
2. Dual boot time fix: ```sudo timedatectl set-local-rtc 0 --adjust-system-clock```
3. Disable gnome software auto start: ```sudo rm /etc/xdg/autostart/org.gnome.Software.desktop```
4. Setting up 1.1.1.1: IPv4: ```1.1.1.1, 1.0.0.1``` | IPv6: ```2606:4700:4700::1111, 2606:4700:4700::1001```
## Setting up repos: 
1. sudo nano /etc/apt/sources.list.d/debian.sources
2. Add these lines:

 ```deb http://deb.debian.org/debian/ trixie main contrib non-free```

 ```deb http://deb.debian.org/debian/ trixie-updates main contrib non-free```

 ```deb http://security.debian.org/debian-security trixie-security main contrib non-free```
