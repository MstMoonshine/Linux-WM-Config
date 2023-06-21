# My i3WM Configuration



This repository contains my personal configuration for i3wm.

**Note:** *The repository is more meant to be a backup rathor than a clone-and-use project.* There are many hard-coded configurations that are never meant to be general, which require manual adjusts to fit each computer and screen.



Configurations for the following software are contained:

- i3: the window manager
- polybar: the status bar
- picom: the compositor
- rofi: the launcher
- kitty: the terminal
- alacritty: another terminal, used when kitty behaves buggy



All software are installed using AUR. I am currently using Manjaro, but they are supposed to work under Arch Linux as well. To use these configurations, copy the contents inside the `config` directory to your `$HOME/.config/`.

---



## i3wm

I am using `i3-gaps-rounded-git`, which provides rounded corner windows.



## Polybar

My customized configuration is modified from the *shades* theme provided by [polybar-themes](https://github.com/adi1090x/polybar-themes).

Before using the configuration, copy the fonts to the system:

```bash
cp -rf config/polybar/fonts ~/.local/share/fonts
```



## Picom

Use the official picom package. Or on devices with AMD processor, use the `picom-jonaburg-git` package.



## Rofi

My rofi configurations are also modified from the [polybar-themes](https://github.com/adi1090x/polybar-themes). There is a sub-directory for the rofi launcher.

After install the configuration files, the corresponding key-binding in i3-config will take effect:

```bash
bindsym $mod+space exec --no-startup-id rofi -no-config -no-lazy-grab -show drun -modi drun -theme ~/.config/rofi/config.rasi
```

Then pressing `$mod+space` should trigger the rofi process.

To add new items into the rofi menu, add desktop descriptors to `$HOME/.local/share/applications`.



### Kitty

I am using a kitty configuration copied from hyprland default configuration, which is based on [sainnhe's forest night theme](https://github.com/sainnhe/forest-night).



 ## Alacritty

Install `nerd-fonts-sf-mono` from AUR first.







