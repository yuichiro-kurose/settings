-----

# vim-plug インストール手順

-----

## 1. `plug.vim` をダウンロード

`vim-plug` をインストールするには、まず以下のコマンドを実行して `plug.vim` をダウンロードします。

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

-----

## 2. `.vimrc` にプラグイン設定を追加

次に、`~/.vimrc` ファイルを開き、以下の形式でプラグイン設定を追加します。`call plug#begin()` と `call plug#end()` の間に、使用したいプラグインを `Plug '...'` の形式で列挙してください。

```vim
" ~/.vimrc
call plug#begin('~/.vim/plugged')

Plug '...'
Plug '...'

call plug#end()
```

-----

## 3. Vim を起動して `:PlugInstall` を実行

設定が完了したら Vim を起動し、コマンドモードで `:PlugInstall` を実行してプラグインをインストールします。

```vim
:PlugInstall
```

-----

## その他便利なコマンド

| コマンド | 説明 |
| :------------- | :--------------------------------- |
| `:PlugInstall` | 新しいプラグインをインストールします。 |
| `:PlugUpdate` | すでにインストールされているプラグインを更新します。 |
| `:PlugClean` | `.vimrc` から削除されたプラグインをアンインストールします。 |
| `:PlugStatus` | プラグインの状態を表示します。 |
