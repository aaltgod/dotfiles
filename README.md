# Setup
## Use EndeavourOS

---
## Hyprland
## 
```
sudo pacman -S hyprland htop alacritty neovim wofi mirage
```

---
## Sddm

```
yay -a sddm-git sddm-theme-astronaut
```

/etc/sddm.conf.d/sddm.conf
```
[Autologin]
# Uncomment it if you need autologin
#User=aalt
#Session=hyprland.desktop

[Theme]
Current=astronaut
```
/etc/sddm.conf.d/hidpi.conf
```
[Wayland]
EnableHiDPI=true
```

```
sudo systemctl enable sddm
sudo systemctl enable --now sddm
```

---
## Swaylock
```
yay -a swaylock-effects
```
Add in ~/.config/hypr/hyrpland.conf
```
bind = $mainMod, L, exec, swaylock --screenshots --clock --indicator --indicator-radius 100 --indicator-thickness 7 --effect-blur 7x5 --effect-vignette 0.5:0.5 --ring-color bb00cc --key-hl-color 880033 --line-color 00000000 --inside-color 00000088 --separator-color 00000000 --grace 2 --fade-in 0.2
```

---
## Hyprpaper
```
yay -a hyprpaper 
```
Add(create if not exists) in ~/.config/hypr/hyrpaper.conf
```
preload = ~/.config/hypr/wallpaper.jpg

#set the default wallpaper(s) seen on inital workspace(s) --depending on the number of monitors used
wallpaper = eDP-1,~/.config/hypr/wallpaper.jpg
```

---
## Mako
```
yay -S mako
```
Add in ~/.config/hypr/hyrpland.conf
```
exec-once=mako
```
---
## Eww
[source](https://github.com/elkowar/eww)

```
yay -S ttf-jetbrains-mono-nerd
fc-cache -fv
```

```
yay -a eww-wayland
mkdir -p .config/eww/{eww.yuck,eww.scss}
```
