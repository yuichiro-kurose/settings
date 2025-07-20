-----

# Arch Linux インストール手順

-----

## Wi-Fi 接続

以下を実行.

```bash
iwctl
station device scan
station device get-networks
station device connect SSID
```

通常、`device` は `wlan0` だ.

-----

## Arch Linux のインストール

以下を実行.

```bash
archinstall
```

-----

## GNOME のインストール

以下を実行.

```bash
pacman -S gnome gnome-tweaks gnome-shell-extensions gdm --needed
systemctl enable gdm.service
```

インストール後、システムを再起動する.

```bash
reboot
```
