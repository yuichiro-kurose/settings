-----

# Arch Linux 日本語入力設定手順

-----

## 必要なパッケージのインストール

以下を実行.

```bash
sudo pacman -S noto-fonts-cjk fcitx5-im fcitx5-mozc
```

-----

## 環境変数の設定

`~/.config/environment.d/im.conf` ファイルを作成し、以下を記述.

```ini
INPUT_METHOD=fcitx
GTK_IM_MODULE=fcitx
QT_IM_MODULE=fcitx
XMODIFIERS=@im=fcitx
```

-----

## セッションごとの Fcitx5 自動起動設定

以下を実行.

```bash
mkdir -p ~/.config/autostart
cp /usr/share/applications/org.fcitx.Fcitx5.desktop ~/.config/autostart/
```

-----

## 再起動

設定を反映させるためにシステムを再起動する.

```bash
reboot
```

-----

## 初回起動後の設定

システム再起動後、`fcitx5-configtool` を使用して **Mozc（日本語入力）** を追加.

-----
