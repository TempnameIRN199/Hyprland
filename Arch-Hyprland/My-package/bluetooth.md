### Delete "pulseaudio"

`sudo pacman -Rns pulseaudio pulseaudio-bluetooth`

### Install "pipewire"

`sudo pacman -S pipewire-pulse`
`systemctl --user enable --now pipewire-pulse`
`reboot`

### Test

pactl list short sinks
