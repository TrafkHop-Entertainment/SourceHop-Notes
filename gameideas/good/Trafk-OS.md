# Things needed to be installed:
* archiso
* Calamares fürs installationsmenü
* grub
* polkit + polkit-gnome
* GPU Treiber (bei installation auswählen)
* vulkan-radeon / vulkan-intel / nvidia-utils
* lib32-mesa + lib32-vulkan-radeon (bzw. Intel/Nvidia-Äquivalent)
* sddm
* hyprland, waybar, hyprpaper, hyprlock, rofi, dunst
* pipewire + pipewire-pulse + pipewire-alsa + wireplumber
* pavucontrol
* xorg-xwayland
* Dolphin (oder was anderes) + dolphin-plugins
* kitty (oder was anderes)
* grim + slurp
* wl-clipboard
* cliphist
* bluez + bluez-utils + blueman
* xdg-desktop-portal-hyprland + xdg-desktop-portal-gtk
* hypridle
* networkmanager +network-manager-applet mit waybyr integration
* peazip
* firefox
* nano
* htop
* imv
* ufw
* qt5ct + qt6ct
* brightnessctl
* playerctl
* sof-firmware
* pipewire-jack
* nwg-look
* kvantum
* gufw
# Optional packages
## Social
* discord
* thunderbird
## Multimedia
* qbittorrent
* makeMKV
* asunder
* handbrake
* vlc + vlc-plugins-all + ffmpeg
## Work
* python
* cmake
* jetbrains-toolbox
* renpy
* bambustudio
* kdenlive
* audacity
* obs-studio
* kolourpaint
* gimp
* qalculate-gtk
* obsidian
* libreoffice
* kate
## drivers
* opentabletdriver
* webcamoid
* openrgb
* flatpak
* yay
  sudo pacman -S --needed base-devel git  
  git clone [https://aur.archlinux.org/yay.git](https://aur.archlinux.org/yay.git "https://aur.archlinux.org/yay.git")  
  cd yay  
  makepkg -si
* webkitgtk2
## other
* fastfetch
* timeshift
* tailscale
* trayscale
* MEGA
  wget https://mega.nz/linux/repo/Arch_Extra/x86_64/megasync-x86_64.pkg.tar.zst && sudo pacman -U "$PWD/megasync-x86_64.pkg.tar.zst"
## Games
* Steam
* Itch
* Heroic
* mangohud
* winetricks wine-staging wine-gecko
* waydroid
* gamemode
* lsfg-vk-git  
### yay:  
* openttd
* supertuxkart-git
* cubyz-bin
* prismlauncher
* airshipper
* srb2
* srb2kart
* [hytale-launcher-bin](https://aur.archlinux.org/packages/hytale-launcher-bin "https://aur.archlinux.org/packages/hytale-launcher-bin")
### flatpak
* flatpak remote-add --if-not-exists flathub 
* flatpak install flathub org.vinegarhq.Sober  
* flatpak install flathub org.vinegarhq.Vinegar
* flatpak install flathub io.mrarm.mcpelauncher
### Emulators (yay):  
* stella
* xemu
* xenia-edge-bin
* [azaharplus-appimage](https://aur.archlinux.org/pkgbase/azaharplus-appimage)
* parallel-launcher  
* cemu  
* dolphin-emu-git  
* mesen
* mgba-qt-git
* bsnes-hd
* melonds
* vita3k-git
* rpcs3-bin
* ppsspp-git
* pcsx2-git
* duckstation-preview-latest-bin
* shadps4-qtlauncher-bin
* kega-fusion
* flycast-git
* virtualboy emulator search!
### Local Disk Games
* Ya can't add them ofc, but the notes don't lie
# Theming to be done:
* Hyprland + co
* GTK-Theme
* Icon-Theme
* Cursor-Theme
* Nerd Font
* Wallpaper
* Grub
* Calamares
* SDDM
* Browser???