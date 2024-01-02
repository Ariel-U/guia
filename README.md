# guia
Este repositorio es solo una ayuda memoria para mi mismo. Necesita mucho trabajo y no está listo para reproducirse en otros sistemas.

# Qué hago despues de instalar una distro?

pequeña guia para no olvidarme. en el futuro quizás convertir esto en un script.

## actualizar mirrors
```
# para arch
sudo reflector --country Worldwide,Brazil,Chile --protocol https --fastest 10 --verbose --save /etc/pacman.d/mirrorlist && sudo pacman -Syy && cat  /etc/pacman.d/mirrorlist"
```
## instalar programas más comunes
```
# apps comunes que instalo siempre:
# Para arch 
sudo pacman -S firefox git micro nextcloud-client neofetch zsh zsh-syntax-highlighting zsh-autocomplete exa flatpak base-devel reflector
sudo pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si # instala Yay
yay -S vital-synth spotify brave -bin
flathub install -y reaper stremio

# otras apps que quizas necesito?
# juegos
sudo pacman -S steam lutris 
yay -S heroic-games-launcher-bin  
flatpak install retroarch

#wine
sudo pacman -S wine winetricks
yay -S install bottles yabridge-bin

# Solo para gnome. Tweaks y extensiones
gnome-tweaks dash-to-dock dash-to-panel arcmenu gsconnect appindicator capitaine-cursors pavucontrol

```

## rescatar dotfiles
```
git clone https://github.com/Ariel-U/setup/ && cd setup && chmod +x setup.sh && ./setup.sh && cd ~ && source .bashrc
chsh -s /bin/zsh
sudo systemctl restart gdm # gnome
sudo systemctl restart sddm # plasma
sudo systemctl restart lightdm # otros
```
## preparar para trabajar con audio
revisar [este](https://github.com/brendaningram/linux-audio-setup-scripts) repo 
