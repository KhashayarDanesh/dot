# dot

Dotfiles and whatnot

## i3 WM Configuration

The i3 configuration directory is `~/.config/i3/`
My current i3 Configuration requires multiple packages to function as intended, which can be installed with these commands:

This setup uses `rofi` as the launcher, `polybar` status bar, `alsamixer` for the volume mizer in the status bar, nm-applet (for the application trey and BT and Wlan selector)

### Keybindings

Shortcuts and Keybindings Map will be added to this repo as a cheatsheet soon, but as a general rule, I have not modified it very much for the time being, so it's similar to i3 Defaults with `ALT` set as `modkey`
and it supports media control tools.

Also, Caps Lock button is set tu be used as the language switcher. (you can find the configuration in the i3 config file itself, search for the keyword `setxkb`)

### installation

You can install all the required packages using this command:

```bash

Archlinux :

sudo pacman -S i3wm nm-applet polybar rofi imagemagick feh xorg-xrandr xorg-xdpyinfo alsa-utils lxappearance-gtk3 network-tools; \
yay -S light betterlockscreen

_______________________________________________________________________

Debian Based Distributions:

sudo apt install i3wm nm-applet polybar rofi lxappearance-gtk3 alsa-utils network-tools

And you should install the light package manuall from this link:
https://github.com/haikarainen/light
```

the windowing system theme, icon pack and cursor theme are intended to be customized using the `lxappearance-gtk3` package.

As we're using betterlockscreen, we have to enable betterlockscren's systemd unit with this command: 

```bash
systemctl enable betterlockscreen@$USER
```

### Inspiration Source

The theme itself is inspired by the old Solaris machine found in [Flynn's Arcade](https://tron.fandom.com/wiki/Flynn%27s_Arcade)

## Polybar Configuration

The polybar configuration is also built to comply with the general idea of the i3WM configuration.

the configuration files should be placed in `~/.config/polybar`

## X Resources Configuration

The .Xresources is responsible for the Xorg additional configuration and passing `Rofi` its configuration and it should reside in ~/.Xresources

In the last line of this configuration is responsible for setting a custom image density to make the setup usable in HiDPI/Retina Displays.

This configuration has not been tested with multi-displays yet, but hopefully it will be tested very soon.

Notice: `I AM NOT RESPONSIBLE FOR YOUR BROKEN COMPUTER, just in case.` `There might be issues with the installation manual, such as forgetting to list dependency packages etc. feel free to contact me in that case or in case of any suggestions`
