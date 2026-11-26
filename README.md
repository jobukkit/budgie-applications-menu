# Applications Menu
[![Translation status](https://l10n.elementary.io/widgets/wingpanel/-/applications-menu/svg-badge.svg)](https://l10n.elementary.io/engage/wingpanel/?utm_source=widget)

This is a fork of the Ubuntu Budgie applications menu that continues to compile and work well on other distributions. Tested on:
- Solus with Budgie 10.10 on Wayland
- Solus with [Rill](https://codeberg.org/lzj15/rill)/[River](https://isaacfreund.com/software/river/) on Wayland
- Void Linux with Budgie 10.9 [on XLibre](https://github.com/xlibre-void/xlibre)
- OpenMandriva with Budgie 10.9 on XLibre

![Screenshot](data/screenshot.png?raw=true)

## Building and Installation

You'll need the following dependencies:
* libgee-0.8-dev
* libgranite-dev >= 6.1.0
* libgtk-3-dev
* libhandy-1-dev >= 0.83.0
* libjson-glib-dev
* libplank-dev
* libswitchboard-2.0-dev
* libunity-dev
* libwingpanel-dev
* libzeitgeist-2.0-dev
* meson
* pkg-config
* valac

Run `meson` to configure the build environment and then `ninja` to build

    meson build --prefix=/usr -Dfor-wayland=true # or false when using XLibre
    cd build
    ninja

To install, use `ninja install`

    sudo ninja install
