# tmux
個人的なtmuxの設定になります．

# 下準備
## Linux
- tmux
- powerline
- xclip
- Meta Key

### tmux
Install:

```
$ sudo add-apt-repository -y ppa:pi-rho/dev
$ sudo apt-get update
$ sudo apt-get install tmux-next
$ sudo ln -s /usr/bin/tmux-next /usr/bin/tmux
```

### powerline

Install:

```
$ pip install powerline-status
$ git clone https://github.com/powerline/fonts.git
$ fonts/install.sh
$ rm -rf fonts
```

インストール後，各種ターミナルのフォントをPowerline仕様のものに変更する．

Configure:

```
$ git clone git@github.com:h3poteto/powerline-config.git ~/.config/powerline
```
### xclip
tmuxのバッファとOSのクリップボードを共有するために使う．

```
$ sudo apt-get install xclip
```


### Meta Key
ペインの移動にMetaキーを使用しているが，通常の日本語キーボードの場合，AltがMetaに対応してしまう．
これをWinキーでMeta入力できるようにする．

`~/.Xmodamp` を作成し，

```
keycode <Win Key Code> = Meta_L
```
とする．`<Win Key Code>` は `xev` を使って調べることができる．

この設定を `~/.zshrc` で読み込む(X Window全体に効かせる必要はないため)．

```bash
xmodmap $HOME/.Xmodmap
```


## MacOS
- tmux
- powerline
- reattach-to-user-namespace

### tmux
Install:

```
$ brew install tmux
```

### powerline

Install:

```
$ pip install powerline-status
$ git clone https://github.com/powerline/fonts.git
$ fonts/install.sh
$ rm -rf fonts
```

インストール後，各種ターミナルのフォントをPowerline仕様のものに変更する．

Configure:

```
$ git clone git@github.com:h3poteto/powerline-config.git ~/.config/powerline
```

### reattach-to-user-namespace
tmuxのbufferとOSの持つコピー&ペーストバッファを共有するために入れておく．

```
brew install reattach-to-user-namespace
```


# 導入

```
$ git clone git@github.com:h3poteto/.tmux.git
$ touch .tmux.conf
```

`.tmux.conf` を以下のように編集する．
```
run-shell "powerline-daemon -q"
source ~/.pyenv/versions/3.6.5/lib/python3.6/site-packages/powerline/bindings/tmux/powerline.conf
source ~/.tmux/tmux.conf
```
