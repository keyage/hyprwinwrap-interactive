# hyprwinwrap-interactive

This is a soft fork of hyprwm/hyprland-plugins that tweaks hyprwinwrap to allow interactivity to be toggled via a dispatcher

# Install

## Install with `hyprpm`

To install these plugins, from the command line run:

```bash
hyprpm update
```

Then add this repository:

```bash
hyprpm add https://github.com/keircn/hyprwinwrap-interactive
```

then enable the desired plugin with

```bash
hyprpm enable hyprwinwrap
```

toggle interactivity with

```bash
hyprctl dispatch hyprwinwrap_toggle
```

Set "new_optimizations" to false in hyprland.conf blur settings if you want tiled windows to render the app instead of your wallpaper when opaque.

If you are using waybar and it gets covered by the app, set "layer" to "top".

See [README.md](./hyprwinwrap/README.md) for configuration examples.

# Contributing

Feel free to open issues and MRs with fixes.

If you want your plugin added here, contact vaxry beforehand.
