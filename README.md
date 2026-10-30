# Touchpad tuner

A small GTK app for Cinnamon on X11. It reads the touchpad, then changes pointer speed, clicking, and scrolling. Settings are saved with Cinnamon and applied right away through xinput.

## What it can change

- Pointer speed
- Tap to click, tap and drag, and whether the touchpad is on
- Click actions: bottom corners, press anywhere, or off
- Scroll direction and two-finger or edge scrolling
- A try-out pad that shows which click arrived and how fast the pointer moved

Press-anywhere mode keeps a one-finger press as a left click, including a press on the bottom edge when the sensor misses the finger. Right click is two fingers pressed down. Middle click is a three-finger tap or a three-finger press.

## Requirements

- Cinnamon on X11
- Python 3 with GTK 3 (`python3-gi`, `python3-cairo`)
- `xinput`

## Install

```sh
install -m 755 touchpad-tune "$HOME/.local/bin/touchpad-tune"
mkdir -p "$HOME/.local/share/applications"
cp touchpad-tune.desktop "$HOME/.local/share/applications/"
update-desktop-database "$HOME/.local/share/applications" 2>/dev/null || true
```

Run it from the menu as **Touchpad tuner**, or run `touchpad-tune`.
