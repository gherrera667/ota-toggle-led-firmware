# ota-toggle-led-firmware

Release artifacts for the `ota_toggle_led` ESP32-C6 demo. This repository holds
firmware binaries only; the source code is not published here.

## What this is

A demo that blinks the on-board LED and updates itself over the air (OTA).
The device checks `manifest.json` for the current version, and if it differs from
the running one, downloads the image it names over HTTPS.

## Layout

```
manifest.json                         current version and where to fetch it
firmware/ota_toggle_led-<version>.bin one image per released version
```

Image filenames include the version, so a stale cache can never serve the wrong
file under an old name. Old versions stay available.

## Using the images

These images are built for the ESP32-C6 and are meant for the demo device. Do not
flash them onto other hardware.

## License

No license is granted. All rights reserved. Downloading these files does not
give you permission to redistribute or reuse them.
