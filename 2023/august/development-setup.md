## Creating a User
`useradd -m <nameofuser>`
## Password for `<nameofuser`
`passwd <nameofuser>`

## Download the X server
`sudo pacman -S xorg-server`

## Download the x-init package
`sudo pacman -S xorg-xinit`

## Create ~/.xinitrc

In `~/.xinitrc` i have to declare which things i want to run on x-server. such as window manager like `dwm` , some daemon like network manager , some status bar etc.

If I have `dwm` installed then i can put in `~/.xinitrc` `exec dwm`

## Then installing a window manager for me its `dwm` . It will come with `st , dmenu `



