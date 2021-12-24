# sex52

controls the logitech x52 pro from Elite Dangerous in linux.  prints cargo, important journal events, and nav route on MFD, toggles the LEDs on button press, and handles other buttons that the linux driver cant (through evdev).

if getting permissions errors, set up a udev rule:

`/etc/udev/rules.d/20-sex52.rules`

`ATTRS{idVendor}=="06a3", ATTRS{idProduct}=="0762", OWNER="[USERNAME]"` *Replace [USERNAME] with your username

then reload:

`udevadm control --reload-rules && udevadm trigger`

run with:

`python sex52`

only tested with python3.
