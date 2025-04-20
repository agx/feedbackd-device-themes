# Device specific feedback themes for Feedbackd

[feedbackd][] provides a DBus daemon (feedbackd) to act on events to provide
haptic, visual and audio feedback. This repository contains the device
specific feedback theme files.

## License

Themes are licensed under the GPLv3+.

## Getting the source

```sh
git clone https://gitlab.freedesktop.org/agx/feedbackd-device-themes
cd feedbackd-device-themes
```

The `main` branch has the current development version.

## Building

This validates the contained themes:

```sh
meson . _build
meson test -v -C _build
```

If you don't want to install the themes you can test a specific theme
using feedbackd's `FEEDBACK_THEME` environment variable.

## Adding a new theme

Steps for adding a new theme

- Add the theme itself to [data/] after performing the above validation.
  Make sure to chain up to the parent theme.
- Mention your device in [debian/control][]
- Update the copyright in [debian/copyright][]
- Submit a merge request to <https://gitlab.freedesktop.org/agx/feedbackd-device-themes/-/merge_requests>

## Getting in Touch

- Issue tracker: <https://gitlab.freedesktop.org/agx/feedbackd-device-themes/-/issues>
- Matrix: <https://matrix.to/#/#phosh:sigxcpu.org>

[feedbackd]: https://gitlab.freedesktop.org/agx/feedbackd
[debian/control]: https://gitlab.freedesktop.org/agx/feedbackd-device-themes/-/blob/main/debian/control#L24
[debian/copyright]: https://gitlab.freedesktop.org/agx/feedbackd-device-themes/-/blob/main/debian/copyright#L11
