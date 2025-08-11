# My-personal-linux-setup

This is inspired by this project which is for fedora but I've made this for small general tweaks: https://github.com/wz790/Fedora-Noble-Setup

1. Make boot times faster: ```sudo systemctl disable NetworkManager-wait-online.service```

2. Dual boot time fix: ```sudo timedatectl set-local-rtc 0 --adjust-system-clock```

3. Disable gnome software auto start: ```sudo rm /etc/xdg/autostart/org.gnome.Software.desktop```

4. Setting up 1.1.1.1: IPv4: ```1.1.1.1, 1.0.0.1``` | IPv6: ```2606:4700:4700::1111, 2606:4700:4700::1001```

## Adding sudo: 

As root

```adduser user```

```adduser user sudo```

### To check if the user is sudo: 

```sudo -l -U user```

## Adding repos: 

```sudo nano /etc/apt/sources.list```

Add these lines: 

```deb http://deb.debian.org/debian/ trixie main contrib non-free```

```deb http://deb.debian.org/debian-security/ trixie-security main contrib non-free```

```deb http://deb.debian.org/debian/ trixie-updates main contrib non-free```

## Setting up flathub

```sudo apt install flatpak```

```sudo apt install gnome-software-plugin-flatpak```

```sudo apt install plasma-discover-backend-flatpak```

```flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo```
