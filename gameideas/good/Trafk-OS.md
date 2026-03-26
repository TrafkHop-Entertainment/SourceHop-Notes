Hey, will eine Linux Distro erstellen!

Diese soll grub sddm hyprland(master) wallpaper waybar rofi dolphin cursertheme calamares und fastfetch customized haben.

Es soll einen gui installer haben, indem man zusätzlich verschiedene paketgruppen mitauswählen kann (inc. yay & flatpak pakete). Rofi soll auch verschiedene softwaregruppen haben, die man wie ordner öffnen kann (soll auch verschachtelt funktionieren). Wenn möglich soll die rofi active windows anzeige auf waybar angezeigt werden und klickbar sein. Alle typischen F Tasten und Laptop Tasten sollen funktionieren. bluetooth, wlan, drucker (inc canon), etc sollen einwandfrei funktionieren.

# Zum selber Installieren
## archinstall
* english
* de de_AT UTF-8
* austria germany US WW
* multilib multilib-testing core-testing extra-testing
* ext4 no home
* Trafk-OS Trafk hopx 123 sudo ja
* minimal
* bluetooth ja audio pipewire print ja
* networkmanager default backend
* Europe/Vienna
* extra Paket: archiso
* exit archinstall
# Nötige Pakete:
sudo pacman -Syy --needed base linux linux-firmware linux-headers bash-completion noto-fonts noto-fonts-emoji ntfs-3g gvfs gvfs-mtp gvfs-smb p7zip unrar zip unzip cups cups-pdf avahi bluez-cups bluez-utils xdg-user-dirs upower acpi acpi_call power-profiles-daemon qt5-wayland qt6-wayland system-config-printer grub polkit-kde-agent sddm vulkan-radeon mesa vulkan-intel hyprland waybar hyprpaper hyprlock rofi dunst pipewire pipewire-pulse pipewire-alsa wireplumber pavucontrol xorg-xwayland dolphin foot grim slurp wl-clipboard cliphist bluez bluez-utils blueman xdg-desktop-portal-hyprland xdg-desktop-portal-gtk hypridle networkmanager network-manager-applet firefox nano htop imv ufw qt5ct qt6ct playerctl sof-firmware pipewire-jack nwg-look kvantum gufw flatpak gparted kate kolourpaint ark fastfetch fuse2 mtools dosfstools nvidia-open nvidia-utils nvidia-settings egl-wayland libva-utils lib32-vulkan-radeon lib32-mesa lib32-vulkan-intel lib32-nvidia-utils brightnessctl dolphin-plugins base-devel git keyd print-manager hplip xdg-user-dirs-gtk qt5-imageformats kimageformats sddm-kcm wget curl noto-fonts-cjk

sudo pacman -S  ttf-jetbrains-mono-nerd

git clone [https://aur.archlinux.org/yay.git](https://aur.archlinux.org/yay.git "https://aur.archlinux.org/yay.git")
cd yay
makepkg -si

yay -S calamares

flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

sudo systemctl enable sddm
sudo systemctl enable NetworkManager
sudo systemctl enable bluetooth
sudo systemctl enable cups.service
systemctl --user enable pipewire pipewire-pulse wireplumber
xdg-user-dirs-update

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
* gimp
* qalculate-gtk
* obsidian
* libreoffice-fresh
## drivers
* opentabletdriver
* webcamoid
* openrgb
  makepkg -si
* webkitgtk2
## other
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
* Hyprland
  ~/.config/hypr/hyprland.conf
* waybar
* rofi
  .config/rofi
* Grub
* Sddm
* Wallpaper
* Dolphin (File Explorer)
* Curser Theme
* Calamares
* fastfetch
## Suchen und Selber Machen
GTK-Theme (und anpassen)