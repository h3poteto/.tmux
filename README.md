# tmux
個人的なtmuxの設定になります．

## 導入

```
$ git clone git@github.com:h3poteto/.tmux.git
$ touch .tmux.conf
```

`.tmux.conf` を以下のように編集する．
```
source "/Users/akirafukushima/.pyenv/versions/3.6.5/lib/python3.6/site-packages/powerline/bindings/tmux/powerline.conf"
source ~/.tmux/tmux.conf
```

## 別途必要になるもの

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
```

Configure:

```
$ git clone git@github.com:h3poteto/powerline-config.git ~/.config/powerline
```

## MacOS
TODO
