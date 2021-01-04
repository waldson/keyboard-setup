# Custom Keyboard Mapping

This setup will:

1. Make a US layout keyboard work like(ish) a BR layout keyboard:
    1. `AltGr+z` becomes `\` and `AltGr+Shift+z` becomes `|`
    2. `Alt+]` becomes `\` and `Alt+Shift+]` becomes `|`
2. Make caps lock work as both control (pressed) and ESC (tapped).
3. Add media key shortcuts:
    1. `AltGr+F1`: Mute
    2. `AltGr+F2`: Volume Down
    3. `AltGr+F3`: Volume Up
    4. `AltGr+F4`: Previous Song
    5. `AltGr+F5`: Play/Pause
    6. `AltGr+F6`: Next Song
4. Add some navigation facilities:
    1. `AltGr+a`: Left
    2. `AltGr+s`: Down
    3. `AltGr+d`:  Right
    4. `AltGr+w`: Up
    5. `AltGr+h`: Home
    6. `AltGr+j`: Page Down
    7. `AltGr+k`: Page Up
    8. `AltGr+l`: End

## Setup

1. Install [Interception Tools](https://gitlab.com/interception/linux/tools)
2. Install [dual-function-keys](https://gitlab.com/interception/linux/plugins/dual-function-keys)
3. Compile and install this code:
    1. `mkdir build && cd build`
    2. `cmake -DCMAKE_BUILD_TYPE=Release ..`
    3. `make`
    4. `sudo make install`
4. Copy `config-files/dual-function-keys.yaml` to  `/etc/dual-function-keys.yaml`
5. Copy `config-files/udevmon.yaml` to `/etc/udevmon.yaml`
6. Copy `config-files/udevmon.service` to `/etc/systemd/system/udevmon.service`
7. Enable service: `sudo systemctl enable --now udevmon.service`

## TO-DO
* [ ] Create an installation script
* [ ] Make right shift becomes `/` and `?`
