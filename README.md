# Manjaro dotfiles
Various dotfiles and settings for my Manjaro Linux installation.

* Scripts for my `dwm` status bar are in `~/.local/bin/statusbar/`
* Wallpaper setting script in `~/.local/bin/setbg`. This script is also used by `dwm` at startup to automatically set the wallpaper and color scheme. See the script for more info.
* Settings for various programs, such as `zsh`, `mpv` and so on, are in `~/.config/`
* Source code for `dwm`, `dwmblocks` (the status bar) and `st` (simple terminal) that I use are in `~/.config/suckless/`
* `dwm`:
    * Version 6.2
    * Patches that I've applied:
        * `fullgaps` - adds gaps between windows and allows to configure them at run-time.
        * `shiftview` - allows the user to rotate the currently selected tag (http://lists.suckless.org/dev/1104/7590.html)
        * `swallow` - adds window swallowing functionality. As an example, starting `mpv` or `sxiv` will now "hide" the terminal window that started that process. This patch helps users spawning a lot of graphical programs from their command line by avoiding cluttering the screen with many unusable terminals.
* `dwmblocks` - modular status bar for dwm (https://github.com/torrinfail/dwmblocks)
* `st` (simple terminal):
    * Version 0.8.3
    * Patches that I've applied:
        * `alpha` - allows the user to have transparent terminals (requires `xcompmgr` or some other X compositor, such as `picom` to be running in the background, the startup script takes care of that)
        * `anysize` - smoothly changes the terminal's window size when adjusting window gaps
        * `scrollback` - allows the user to scrollback the terminal output. I've also applied the `scrollback-mouse` patch so that I can scroll the terminal output back and forth using Shift and mouse wheel (by default)
* Rule, which allows setting the backlight by any user in the `video` group without requiring root access is in `/etc/udev/rules.d/90-backlight.rules`
* `dwm` startup script in `/usr/local/bin/start-dwm.sh`
* Session configuration for `dwm` in `/usr/share/xsessions/dwm.desktop`. This allows setting the environment I want to log in to (`dwm` or KDE) at my login prompt.
* Fonts that are required:
    * Liberation Mono (for `dwm` and `st`). Should be installed by default
    * Helvetica Neue (for `mpv` subtitles). To use a different font, replace `sub-font` in `~/.config/mpv/mpv.conf`

# Screenshots (will probably get out of date soon)
## KDE
-- add screenshot for KDE here
## dwm
-- add dwm screenshot here