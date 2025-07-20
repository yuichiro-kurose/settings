-----

# vim-plug インストール手順

-----

## 1. `plug.vim` をダウンロード

以下を実行.

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

-----

## 2. `.vimrc` にプラグイン設定を追加

`~/.vimrc` ファイルを開き、以下の形式でプラグイン設定を追加.`call plug#begin()` と `call plug#end()` の間に、使用したいプラグインを `Plug '...'` の形式で列挙.

```vim
call plug#begin('~/.vim/plugged')

Plug '...'
Plug '...'

call plug#end()
```

-----

## 3. Vim を起動して `:PlugInstall` を実行

Vim を起動し、コマンドモードで `:PlugInstall` を実行してプラグインをインストール.

```vim
:PlugInstall
```

-----

## その他便利なコマンド

| コマンド | 説明 |
| :------------- | :--------------------------------- |
| `:PlugInstall` | 新しいプラグインをインストール. |
| `:PlugUpdate` | すでにインストールされているプラグインを更新. |
| `:PlugClean` | `.vimrc` から削除されたプラグインをアンインストール. |
| `:PlugStatus` | プラグインの状態を表示. |
