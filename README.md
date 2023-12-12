Armbian SystemD networking guideline
====================================

Commands:
- Merge this repo to `/`
- Update SSID and password in `/etc/wpa_supplicant/wpa_supplicant-wlan0.conf`
- Update SSID and password in `/etc/wpa_supplicant/wpa_supplicant-wlan1.conf`
- `apt purge netplan.io network-manager`
- `apt install -y avahi-daemon`
- `systemctl enable wpa_supplicant@wlan0.service`
- `systemctl enable wpa_supplicant@wlan1.service`
- `systemctl start wpa_supplicant@wlan0.service`
- `systemctl start wpa_supplicant@wlan1.service`
- `systemctl unmask systemd-networkd`
- `systemctl enable systemd-networkd`
- Reboot
