### Arch rice in Gnome
- Configure pacman
    sudo vim /etc/pacman.conf
    Add `Color` and `ILoveCandy`
- Install bat, exa
    Use alias and source .bashrc
- Install oh-my-bash
    `agnoster` theme
    `alias cat="bat"`
    `alias ls="exa"`
    `alias vim="nvim"`
    `export EDITOR="vim"`
- Install neovim 
    Clone [kickstart.nvim](https://github.com/Parz1val02/kickstart.nvim) into ~/.config/nvim
- Install oh-my-tmux
- Install alacritty
- Install neofetch, cmatrix, cava
- Catpuccin modded theme for user theme and legacy applications (configure in tweaks)
    This themes allows to have the transparent topbar 
    Copy to ~/.themes 
- Install a nerd font from aur (ComicShannsMono Nerd Font)
- Install icons (papirus)
    `wget -qO- https://git.io/papirus-icon-theme-install | DESTDIR="$HOME/.icons" sh`
    Copy to ~/.icons
### Gnome extensions
- Aylur's Widgets
- Blur my Shell
- Logo menu
- Top bar organizer
- User Themes
- Vitals
- Space bar
- App hider
- Forge for tiling (not necessary for now)
### General recommendations
- Install yay
    `git clone https://aur.archlinux.org/yay.git`
    `makepkg -si`
- Refresh pacman mirrorlist
    `sudo pacman -S reflector`
    `sudo systemctl enable reflector.timer`
- Automatic cleaning the package cache
    `sudo pacman -S pacman-contrib`
    `sudo systemctl enable paccache.timer`
- Enable NTP (Network time protocol)
    Configure /etc/systemd/timesyncd.conf
    Start and enable systemd-timesyncd
- Enable periodic trim for the ssd
    Check TRIM support
	`lsblk --discard`
    Start and enable fstrim.timer
- Instal ufw
    Default settings are fine (deny incoming, allow outgoing connections)

I need swap file
I need to start making backups
I need to start making shell scripts
