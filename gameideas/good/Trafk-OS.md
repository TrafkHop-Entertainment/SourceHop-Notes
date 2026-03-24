# Things needed to be installed:
* archiso
* grub
* polkit + polkit-gnome
* GPU Treiber (bei installation auswählen)
* amd / intel / nvidia / VM
  mesa vulkan-radeon lib32-mesa lib32-vulkan-radeon
  mesa vulkan-intel lib32-mesa lib32-vulkan-intel
  nvidia nvidia-utils lib32-nvidia-utils
  mesa lib32-mesa virtualbox-guest-utils
* sddm
* hyprland, waybar, hyprpaper, hyprlock, rofi, dunst
* pipewire + pipewire-pulse + pipewire-alsa + wireplumber
* pavucontrol
* xorg-xwayland
* Dolphin
* foot
* grim + slurp
* wl-clipboard
* cliphist
* bluez + bluez-utils + blueman
* xdg-desktop-portal-hyprland + xdg-desktop-portal-gtk
* hypridle
* networkmanager +network-manager-applet mit waybyr integration
* firefox
* nano
* htop
* imv
* ufw
* qt5ct + qt6ct
* playerctl
* sof-firmware
* pipewire-jack
* nwg-look
* kvantum
* gufw
* flatpak
* gparted
## AFTER THAT ALL
* yay
  sudo pacman -S --needed base-devel git  
  git clone [https://aur.archlinux.org/yay.git](https://aur.archlinux.org/yay.git "https://aur.archlinux.org/yay.git")  
  cd yay
  makepkg -si
* calamares (yay)
* brightnessctl
* dolphin-plugins
* flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
* virtio-win (yay)
## AFTER THAT
sudo systemctl enable sddm
sudo systemctl enable NetworkManager
sudo systemctl enable bluetooth
systemctl --user enable pipewire pipewire-pulse wireplumber
mkdir -p ~/.config/hypr
cp /usr/share/hyprland/hyprland.conf ~/.config/hypr/hyprland.conf
# Optional packages
## Social
* discord
* thunderbird
## Multimedia
* qbittorrent
* makemkv + makemkv-libaacs
* asunder
* handbrake
* vlc + vlc-plugins-all + ffmpeg
## Work
* python
* cmake
* jetbrains-toolbox
* renpy
* bambustudio-bin
* kdenlive
* audacity
* obs-studio
* kolourpaint
* gimp
* qalculate-gtk
* obsidian
* libreoffice-fresh
* kate
## drivers
* opentabletdriver
* webcamoid
* openrgb
  makepkg -si
* webkitgtk2
* peazip
## other
* fastfetch
* timeshift
* tailscale
* trayscale
* MEGA
  wget https://mega.nz/linux/repo/Arch_Extra/x86_64/megasync-x86_64.pkg.tar.zst && sudo pacman -U "$PWD/megasync-x86_64.pkg.tar.zst"
## Games
* steam
* itch-bin
* heroic-games-launcher-bin
* mangohud-git
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
* sudo pacman -S virt-manager qemu-full libvirt dnsmasq
  sudo systemctl enable --now libvirtd
  sudo usermod -aG libvirt $USER
### Local Disk Games
* Ya can't add them ofc, but the notes don't lie
# Theming to be done:
## Selber Machen:
* Hyprland und co
* Grub
* Sddm
* Wallpaper
* Dolphin (File Explorer)
* Curser Theme
* Calamares
## Suchen
GTK-Theme (und anpassen)
Icon-Theme
Nerd Font