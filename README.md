# Custom Keyboard Mapping

This setup will:

1. Make a US layout keyboard work like(ish) a BR layout keyboard;
2. Make caps lock work as both control (pressed) and ESC (tapped).

## Setup

1. Install [Interception Tools](https://gitlab.com/interception/linux/tools)
2. Install [dual-function-keys](https://gitlab.com/interception/linux/plugins/dual-function-keys)
3. Compile and install this code:
    1. `mkdir build && cd build`
    2. `cmake -DCMAKE_BUILD_TYPE=Release ..`
    3. `make`
    4. `sudo make install`
4. Copy `dual-function-keys.yaml`  `/etc/dual-function-keys.yaml`
5. Copy `udevmon.yaml` to `/etc/udevmon.yaml`
6. Copy `udevmon.service` to `/etc/systemd/system/udevmon.service`
7. Enable service: `sudo systemctl enable --now udevmon.service`
