# arch-defaults

### Rank the fastet 20 German Mirrors by speed and apply them

`url -s "https://www.archlinux.org/mirrorlist/?country=DE&protocol=https&use_mirror_status=on" | sed -e 's/^#Server/Server/' -e '/^#/d' | rankmirrors -n 20 - > /etc/pacman.d/mirrorlist`
