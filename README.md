# wayland-mouse-mapper
Fork of mathportillo's wayland-mouse-wrapper, specific to my system.

## Buttons
These are just the default settings, you can customize them at the start of the mousemapper.sh script.

- Forward: Move to workspace above  (Super+Page up)
- Back: Move to workspace below  (Super+Page down)

## Prerequisites
The script depends on the following executables being available in your PATH:
- libinput
- evemu

to install those just run the following command (with root privileges):
```
dnf -y install libinput evemu
```

## Usage
Run the following command (with root privileges):
```
./mousemapper.sh
```

## Installation (start at boot)
Run the following commands (with root privileges):
```
cp mousemapper.sh /usr/local/bin/mousemapper
cp mousemapper.service /usr/lib/systemd/system/
systemctl enable mousemapper.service
```
