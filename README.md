# Dotfiles Hyprland

Mis archivos de configuración para Hyprland y aplicaciones relacionadas.

## Contenido

- **Hyprland** - Compositor de ventanas para Wayland
- **Waybar** - Barra de estado
- **Rofi** - Lanzador de aplicaciones
- **Kitty** - Emulador de terminal

## Requisitos

- [Hyprland](https://hyprland.org/)
- [Waybar](https://github.com/Alexays/Waybar)
- [Rofi](https://github.com/davatorium/rofi)
- [Kitty](https://sw.kovidgoyal.net/kitty/)
- [GNU Stow](https://www.gnu.org/software/stow/)

## Instalación

```bash
# Clonar el repositorio
git clone git@github.com:pabloreina97/dotfiles-hypr.git ~/dev/lab/dotfiles-hypr

# Entrar al directorio
cd ~/dev/lab/dotfiles-hypr

# Crear symlinks con stow (-t ~ indica que el target es el home)
stow -t ~ hypr waybar rofi kitty
```

Para instalar solo algunos componentes:

```bash
stow -t ~ hypr      # Solo Hyprland
stow -t ~ waybar    # Solo Waybar
stow -t ~ rofi      # Solo Rofi
stow -t ~ kitty     # Solo Kitty
```

## Estructura

```
dotfiles-hypr/
├── hypr/.config/hypr/
│   ├── hyprland.conf
│   ├── hyprlock.conf
│   ├── hypridle.conf
│   ├── monitors.conf
│   ├── workspaces.conf
│   ├── scripts/
│   └── UserConfigs/
├── waybar/.config/waybar/
│   ├── config
│   ├── style.css
│   └── configs/
├── rofi/.config/rofi/
│   ├── config.rasi
│   └── themes/
└── kitty/.config/kitty/
    ├── kitty.conf
    └── kitty-themes/
```

## Desinstalar

Para eliminar los symlinks:

```bash
cd ~/dev/lab/dotfiles-hypr
stow -t ~ -D hypr waybar rofi kitty
```
