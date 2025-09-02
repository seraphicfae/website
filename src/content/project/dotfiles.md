---
title: 'Dotfiles'
description: 'No place like ~'
pubDate: 'May 23 2025'
heroImage: '/assets/dotfiles-hero.png'
---

Thanks to:
- <u>[LinuxMobile](https://github.com/linuxmobile)</u> for the base config
- <u>[Catppuccin](https://github.com/catppuccin)</u> for the amazing themes
- <u>[Adi1090x](https://github.com/adi1090x/rofi/)</u> for the incredible Rofi setup

---

## Showcase

<video controls width="100%" style="max-width: 1080px;">
  <source src="https://github.com/user-attachments/assets/28afbcf3-c731-4860-99d6-e5372815b158" type="video/mp4">
  Your browser doesn’t support HTML5 video.
</video>

---

## Quick Install:
> **Don't run random scripts blindly.**

```bash
git clone https://github.com/seraphicfae/dotfiles
cd hyprland-dotfiles
./setup.sh
```

---

<br>

## Manual Install:

<br>

### Dependencies

```bash
paru -S bluez bluez-utils blueman cava fastfetch ffmpegthumbnailer grim gvfs gvfs-mtp hyprland hyprlock hyprpicker
kitty mako mission-center mpv mtpfs nautilus-open-any-terminal network-manager-applet networkmanager noto-fonts-cjk
noto-fonts-emoji noto-fonts-extra nwg-look obs-studio papirus-icon-theme pavucontrol qt5-wayland qt6-wayland rofi
sddm sddm-theme-catppuccin slurp starship swww ttf-jetbrains-mono-nerd viewnior waybar wl-clipboard xdg-desktop-portal
xdg-desktop-portal-gtk xdg-desktop-portal-hyprland xdg-user-dirs xorg-xwayland zed zsh && rm -rf ~/paru
```
<br>


#### Steps
```bash
cd dotfiles
cp -r .config/* ~/.config/
mkdir -p ~/.icons ~/.themes
cp -r .icons/* ~/.icons/
cp -r .themes/* ~/.themes/
```

<br>

#### Finalizing
```bash
sudo systemctl enable NetworkManager bluetooth sddm
echo -e "[Theme]\nCurrent=catppuccin-mocha" | sudo tee /etc/sddm.conf
chsh -s /usr/bin/zsh
export ZDOTDIR="$HOME/.config/zsh
reboot
```

---
<br>

## FAQ / Common Issues
**My temperature module doesn’t appear in the waybar?** \
Look in waybar and set it to your correct thermal zone.

**MPRIS module is empty** \
It only shows when media is playing.

**My icons look weird/dont show** \
With your package manager, download JetBrainsMono Nerd Font.
