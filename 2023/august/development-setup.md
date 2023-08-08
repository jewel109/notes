## Creating a User
`useradd -m <nameofuser>`
## Password for `<nameofuser>`
`passwd <nameofuser>`

## Download the X server
`sudo pacman -S xorg-server`

## Download the x-init package
`sudo pacman -S xorg-xinit`

## My all package that downloaded through `pacman` will be here.
```
$ sudo pacman -S xorg-server xorg-xinit git font-manager
```

## After installing git make sure to clone my `git --bare ` repo.
 ```
$ git clone --separate-git-dir=$HOME/.dotfiles https://github.com/anandpiyer/.dotfiles.git tmpdotfiles # here my repo will be come
$ rsync --recursive --verbose --exclude '.git' tmpdotfiles/ $HOME/
$ rm -r tmpdotfiles
 
```
[link of the author](https://www.anand-iyer.com/blog/2018/a-simpler-way-to-manage-your-dotfiles.html)

## Git credentials saving
$ `git config --global credential.helper 'cache --timeout=3600'`

## Git editor set to nvim
$ `git config --global core.editor "nvim"`
## Though my all config will linked up through git bare repo . I will explain all of this in here.

## Creating ~/.xinitrc

In `~/.xinitrc` i have to declare which things i want to run on x-server. such as window manager like `dwm` , some daemon like network manager , some status bar etc.

If I have `dwm` installed then i can put in `~/.xinitrc` `exec dwm`

## Then installing a window manager for me its `dwm` . It will come with `st , dmenu `
## For auto starting `dwm` after login making sure to run ` startx ` in `~/.bash_profile` ok.

```
$ #
$ # ~/.bash_profile
$ #
$ if [[ -z $DISPLAY ]] && [[ $(tty) = /dev/tty1 ]]; then
$ startx
$ fi
```

## Then setup local time 

```
$ timedatectl list-timezones # list of time zones
$ timedatectl set-timezone Asia/Dhaka
$ 
```
## installing font and font-viewer
```
$ fc-cache # will update the font
$ fc-cache # will show default fonts
$ fc-list # list of installed fonts
$ 
$ # we need font-manager to view font
font-manager

```



