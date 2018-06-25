# tmux
個人的なtmuxの設定になります．

## 導入

```
$ git clone git@github.com:h3poteto/.tmux.git
$ touch .tmux
```

`.tmux.conf` を以下のように編集する．
```
source "/Users/akirafukushima/.pyenv/versions/3.6.5/lib/python3.6/site-packages/powerline/bindings/tmux/powerline.conf"
source ~/.tmux/tmux.conf
```

## 別途必要になるもの

- powerline
- reattach-to-user-namespace (for MacOS)

