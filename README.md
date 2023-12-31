# Arch install with gnome
- Configure pacman<br/>
    - In /etc/pacman.conf:<br/>
	- `Color`<br/>
	- `ILoveCandy`<br/>
- Install bat, exa<br/>
    - Use alias and source .bashrc<br/>
- Install oh-my-bash<br/>
    - In ~/.bashrc:<br/>
	- `OSH_THEME="agnoster"`<br/>
    	- `alias cat="bat"`<br/>
    	- `alias ls="exa"`<br/>
    	- `alias vim="nvim"`<br/>
    	- `export EDITOR="vim"`<br/>
    	- `neofetch`<br/>
- Install neovim <br/>
    - Clone [kickstart.nvim](https://github.com/Parz1val02/kickstart.nvim) into ~/.config/nvim<br/>
- Install oh-my-tmux, alacritty, neofetch, cmatrix, cava<br/>
    - Copy /alacritty/alacritty.yaml to ~/.config/alacritty/
    - Copy /neofetch/config.conf to ~/.config/neofetch/
- Catpuccin modded theme for user theme and legacy applications (configure in tweaks)<br/>
    - This themes allows to have the transparent topbar <br/>
    - Copy to /Catpuccin/ ~/.themes <br/>
- Install a nerd font from aur (ComicShannsMono Nerd Font)<br/>
- Install icons (papirus)<br/>
    - `wget -qO- https://git.io/papirus-icon-theme-install | DESTDIR="$HOME/.icons" sh`<br/>
    - Copy to ~/.icons<br/>
- Wallpaper: Use variety to dynamically change wallpapers<br/>

## Gnome extensions
- Aylur's widgets<br/>
- Blur my shell<br/>
- Logo menu<br/>
- Top bar organizer<br/>
- User themes<br/>
- Vitals<br/>
- Space bar<br/>
- App hider<br/>
- Dash to dock <br/>
- Rounded window corners <br/>

## General recommendations
- Install yay<br/>
    - `git clone https://aur.archlinux.org/yay.git`<br/>
    - `makepkg -si`<br/>
- Refresh pacman mirrorlist<br/>
    - `sudo pacman -S reflector`<br/>
    - `sudo systemctl enable reflector.timer`<br/>
    - `sudo systemctl start reflector.timer`<br/>
- Automatic cleaning the package cache<br/>
    - `sudo pacman -S pacman-contrib`<br/>
    - `sudo systemctl enable paccache.timer`<br/>
    - `sudo systemctl start paccache.timer`<br/>
- Enable NTP (Network time protocol)<br/>
    - Configure /etc/systemd/timesyncd.conf<br/>
    - Start and enable systemd-timesyncd<br/>
- Enable periodic trim for the ssd<br/>
    - Check TRIM support<br/>
	- `lsblk --discard`<br/>
    - Start and enable fstrim.timer<br/>
- Install ufw<br/>
    - Default settings are fine (deny incoming, allow outgoing connections)<br/>
- Install windows fonts xd<br/>

## Firefox CSS
- In about:config<br/>
    - Change `toolkit.legacyUserProfileCustomizations.stylesheets` to **true**<br/>
- In about:profiles<br/>
    - Navigate to the default profile's root directory and copy the chrome directory<br/>
- userContent.css to change the home page.<br/>
- Wallpaper: [Shooting Star](https://imgur.com/a/8RKmstf)<br/>

#### Todo
>I need swap file<br/>
>I need to start making backups<br/>
>I need to start making shell scripts<br/>
>LTS Kernel<br/>
