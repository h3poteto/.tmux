# tmux
個人的なtmuxの設定になります．

# 下準備

- powerline
- reattach-to-user-namespace (for MacOS)


## Ubuntu
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

## MacOS
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
