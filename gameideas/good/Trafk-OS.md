Hey, will eine Linux Distro erstellen!

Diese soll grub sddm hyprland(master) wallpaper waybar rofi dolphin cursertheme calamares und fastfetch customized haben. und so hald.

Es soll einen gui installer haben, indem man zusätzlich verschiedene paketgruppen mitauswählen kann (inc. yay & flatpak pakete). Rofi soll auch verschiedene softwaregruppen haben, die man wie ordner öffnen kann (soll auch verschachtelt funktionieren). Wenn möglich soll die rofi active windows anzeige auf waybar angezeigt werden und klickbar sein. Alle typischen F Tasten und Laptop Tasten sollen funktionieren. bluetooth, wlan, drucker (inc canon), etc sollen einwandfrei funktionieren.

Das sind meine Notizen dazu und was ich schon hab. Wie findest du es bis jetzt?

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
* 
* sudo pacman -S papirus-icon-theme
* 
 * Clay (icon theme)
   Installation : In Home folder
   Make folder .icons in your home folder Download the tar file and extract in it In terminal run command ~$ gtk-update-icon-cache ~/.icons/namefile (ex : Clay) OR
   In Root folder
   Download the tar file, copy and extract it in /usr/share/icons (can use GUI via file manager as Root or command line) In terminal run command ~$ sudo gtk-update-icon-cache /usr/share/icons/namefile (ex : Clay)

# Nötige Pakete:
sudo pacman -Syy --needed linux linux-firmware linux-headers bash-completion noto-fonts noto-fonts-emoji ntfs-3g gvfs gvfs-mtp gvfs-smb p7zip unrar zip unzip cups cups-pdf avahi bluez-cups bluez-utils xdg-user-dirs power-profiles-daemon qt5-wayland qt6-wayland system-config-printer grub hyprpolkitagent polkit sddm vulkan-radeon mesa vulkan-intel hyprland waybar hyprpaper hyprlock rofi dunst pipewire pipewire-pulse pipewire-alsa wireplumber pavucontrol xorg-xwayland dolphin kitty grim slurp wl-clipboard cliphist bluez bluez-utils blueman xdg-desktop-portal-hyprland xdg-desktop-portal-gtk hypridle networkmanager network-manager-applet firefox nano htop imv ufw nwg-look kvantum playerctl sof-firmware pipewire-jack gufw flatpak gparted kate kolourpaint ark fastfetch fuse2 mtools dosfstools nvidia-open-dkms nvidia-utils nvidia-settings egl-wayland lib32-vulkan-radeon lib32-mesa lib32-vulkan-intel lib32-nvidia-utils brightnessctl dolphin-plugins base-devel git keyd print-manager hplip xdg-user-dirs-gtk qt5-imageformats kimageformats sddm-kcm wget curl noto-fonts-cjk pipewire-audio noise-suppression-for-voice qt5-multimedia qt6-multimedia upower ttf-jetbrains-mono-nerd breeze breeze-gtk os-prober jq vlc vlc-plugins-all ffmpeg gwenview kio-admin qt5ct qt6ct kde-cli-tools plymouth xorg-xcursorgen

git clone [https://aur.archlinux.org/yay.git](https://aur.archlinux.org/yay.git "https://aur.archlinux.org/yay.git")
cd yay
makepkg -si

yay -S calamares xwaylandvideobridge

flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

sudo systemctl enable sddm NetworkManager bluetooth cups.service avahi-daemon keyd bluetooth.service ufw

systemctl --user enable pipewire pipewire-pulse wireplumber
xdg-user-dirs-update
sudo grub-mkconfig -o /boot/grub/grub.cfg

mkdir -p ~/.config/hypr
cp /usr/share/hyprland/hyprland.conf ~/.config/hypr/hyprland.conf

# Optional packages (alle in extra skripts packen)
## Social
* discord
* thunderbird
## Multimedia
* qbittorrent
* makemkv + makemkv-libaacs (yay)
* asunder
* handbrake
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
* cnijfilter2 (yay)
## other
* timeshift
* tailscale
* trayscale
* MEGA
  wget https://mega.nz/linux/repo/Arch_Extra/x86_64/megasync-x86_64.pkg.tar.zst && sudo pacman -U "$PWD/megasync-x86_64.pkg.tar.zst"
* archiso (dev option, inc archiso folder in home)
## Games
* steam
* itch-bin
* heroic-games-launcher-bin
* mangohud
* winetricks wine-staging wine-gecko wine-mono
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
* vbam-wx
* sudo pacman -S virt-manager qemu-full libvirt dnsmasq
  sudo systemctl enable --now libvirtd
  sudo usermod -aG libvirt $USER
### Local Disk Games
* Ya can't add them ofc, but the notes don't lie
# Theming to be done:
* Hyprland
* waybar
* rofi (Done)
* Grub
* Sddm
* Wallpaper
* Dolphin (File Explorer)
* Curser Theme (Done)
* Calamares
* fastfetch (Done)
* breeze-Theme anpassen
* Skripte fürs installieren machen und so
* hyprlock (Done)
* plymouth
* (Bonus:) Ollama KI

### "Fertig" & Was fehlt:
* #### Hyprland (FERTIG)
  hat einen leuchtendgelben schatten, keinen rand, keine rundung und 15px abstand(innen). Dwindle und Master mit Keybinds die linke hand benutzen und gute maus support.

* #### Rofi (FERTIG)
  Rofi hat 2 Menüs: app-menu und power-menu
  in power gibts eine suchleiste und 6 auswahömöglichkeiten in einem 3x2 grid
  killactive(mit exit sign icon, selbstgemacht, 3d), shutdown, reboot, lock, suspend, logout
  in app gibts ein 4x3 grid.
  wenn man nix eingibt, dann sieht man 12 ordner von denen 10 selbst eingerichtet sind, also die kategorien. 11 und 12 sind anders: 11 ist "other programs", das ist einfach drun ohne sachen die schon in den anderen 10 ordnern drinnen sind und 12 ist das gleiche mit run
  Es werden auch automatisch icons gezogen und diese werden groß mittig plaziert, darunter der text!
  Ein Element ist eine Trafkblase, eine Lila Seifenartige Blase, dunkellilablau. Alles in Blender modelliert. Wenn man eine sache anvisiert, dann leutet diese blase vom inneren aus gelblich (mana, Kraft).
  Die Suchleiste ist eine Gestreckte Version Davon
  
* #### hyprpaper
  braucht noch mehr bilder UND ein opt bg skript UND einfach noch verbessern
* #### hyprlock
  wem mach ich was vor, ist nur ki generiert als template, MACHS SELBER DU FAULE SEMMEL
* #### Trafk-OS_Cursor (FERTIG)
  Es ist ein 45px low res blender render von einer "cartoon" hand mit outline. Hat 2 open hands, pointer, text, grab, resize, Xdenied und ne 9 frame wait animation
# Was bis jetzt zum übernehmen wäre
  
  ~/.config
  
  /usr/share/icons

~/.local/share/icons  

etc/os-release
etc/issue
etc/os-release.trafk
usr/share/libalpm/hooks/trafktux-logo.hook
etc/default/grub
etc/hostname

~/archiso   (optionale option, für mich damit ich selber wieder das kompilieren kann, wenn ich was ändern will wenn ich nicht mehr einen vm benutze)


  In Calamares, ka wie das genau geht, aber ich denke mir das es ähnlich wie in archinstall bereits voreingestelltes gibt, language, services, repo server für pacman, etc. Also Archiso hald oder so ka...