-----

# Arch Linux インストール手順

-----

## Wi-Fi 接続

Wi-Fi に接続するには、以下のコマンドを実行します。

```bash
iwctl
station device scan
station device get-networks
station device connect SSID
```

通常、`device` は `wlan0` です。

-----

## GNOME のインストール

GNOME デスクトップ環境をインストールするには、以下のコマンドを実行します。

```bash
pacman -S gnome gnome-tweaks gnome-shell-extensions gdm --needed
systemctl enable gdm.service
```

インストール後、システムを再起動します。

```bash
reboot
```
