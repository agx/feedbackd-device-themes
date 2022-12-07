Device specific feedback themes for Feedbackd
=============================================

[feedbackd][] provides a DBus daemon (feedbackd) to act on events to provide
haptic, visual and audio feedback. This repository contains the device
specific feedback theme files.

## License

Themes are licensed under the GPLv3+.

## Getting the source

```sh
git clone https://source.puri.sm/Librem5/feedbackd-device-themes
cd feedbackd-device-themes
```
The `main` branch has the current development version.

## Building
This validates the contained themes:

```sh
meson . _build
ninja -C _build
```

If you don't want to install the themes you can test a specific theme
using feedbackd's `FEEDBACK_THEME` environment variable.

[feedbackd]: https://source.puri.sm/Librem5/feedbackd
