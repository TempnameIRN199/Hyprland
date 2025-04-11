
`base` - *базовая система*
`base-devel` - *утилиты для сбора софта из исходников*
`linux` - *ядро*
`linux-firmware` - *прошивки для ядра* 
`linux-headers` - *хэдэры для ядра*

`hyprland` - *окружение рабочего пространства*
`hyprpaper` - *управление обоями рабочего стола*
`hyprpicker` - *инструмент для выбора цвета*
`xdg-desktop-portal-hyprland` - *интеграция с приложениями*
`swaylock` - *инструмент для блокировки экрана*
`grim` - *утилита для создания скриншотов*
`slurp` - *утилита для выбора области скриншота в связке с* `grim`
`waybar` - *верхняя панель для отображения состояния системы*

`git`
`sudo`
`man-db` - *помощник в терминале*
`kitty` - *терминал*
`bash-completion` - *авто-фил для консоли*
`nano` - *текстовый редактор*
`vim` - *текстовый редактор*

`firefox` - *браузер*

`pipewire` - *аудиофреймворк*

`intel-ucode` - *драйвер на процессор*

`wayland` - *для взаимодействия приложений с дисплеем*
`xorg-xwayland` - *для работы X11 приложений*

`tlp` - *оптимизация энергопотребления*
**ИЛИ**
`power-profiles-daemon` - *переключение между режимами питания*

`acpi` - *мониторинг батареи*
`brightnessctl` - *регулировака яркости через консоль*

**Шрифты**
`noto-fonts`
`ttf-jetbrains-mono`
`ttf-font-awesome`

`grub` - *пакетный менеджер*
`sddm` - *дисплейный менеджер*
`ntfs-3g` - *чтение NFTS разделов для совместимости файловой системы с Windows*

`efibootmgr` - *утилита для работы с пунктами EFI*
`networkmanager` - *для интернета*
`nvidia` - *проприетарный драйвер NVIDIA*
`bluez` - *блютуз*
`bluez-utils` - *блютуз*
`helvum` - *управление микрофоном*

```
pacstrap /mnt base base-devel linux linux-firmware linux-headers hyprland hyprpaper hyprpicker xdg-desktop-portal-hyprland swaylock grim slurp waybar git sudo man-db kitty bash-completion nano vim firefox pipewire intel-ucode wayland xorg-xwayland acpi brightnessctl noto-fonts ttf-jetbrains-mono ttf-font-awesome sddm ntfs-3g efibootmgr networkmanager nvidia bluez bluez-utils helvum tlp || power-profiles-daemon
```