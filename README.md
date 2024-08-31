# Manage dotfiles with bare git

Following [this guide](https://wiki.archlinux.org/title/Dotfiles)

## setup

```sh
git init --bare ~/.dotfiles
alias dotfiles='/usr/bin/git --git-dir="$HOME/.dotfiles/" --work-tree="$HOME"'
dotfiles config status.showUntrackedFiles no

```

## replicate to new machine

```sh
git clone --bare git@github.com:JXNCTED/dotfiles.git $HOME/.dotfiles
alias dotfiles='/usr/bin/git --git-dir="$HOME/.dotfiles/" --work-tree="$HOME"'
dotfiles checkout
dotfiles config --local status.showUntrackedFiles no
```


