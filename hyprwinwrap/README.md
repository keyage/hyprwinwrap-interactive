# hyprwinwrap

Clone of xwinwrap for Hyprland with interactivity toggle support.

## Configuration

```ini
plugin {
    hyprwinwrap {
        # class is an EXACT match and NOT a regex!
        class = kitty-bg

        # you can also match by title (exact match)
        # title = my-bg-window

        # position as percentage of monitor (default: 0, 0)
        pos_x = 0
        pos_y = 0

        # size as percentage of monitor (default: 100, 100)
        size_x = 100
        size_y = 100
    }
}

# Bind toggle to a key
bind = SUPER, B, hyprwinwrap:toggle
```

### Partial coverage example

To have the background window cover only part of the screen:

```ini
plugin {
    hyprwinwrap {
        class = kitty-bg
        pos_x = 25
        pos_y = 30
        size_x = 40
        size_y = 70
    }
}
```

## Dispatchers

| Dispatcher | Description |
|------------|-------------|
| `hyprwinwrap:toggle` | Toggle interactivity for all background windows |
| `hyprwinwrap:show` | Make all background windows interactable and focus them |
| `hyprwinwrap:hide` | Hide all background windows (render in background only) |
| `hyprwinwrap_toggle` | Legacy alias for `hyprwinwrap:toggle` |

