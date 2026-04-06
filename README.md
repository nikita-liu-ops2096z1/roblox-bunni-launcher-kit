# 🎮 roblox-bunni-launcher-kit

[![tool](https://img.shields.io/badge/tool-MIT-green?style=flat-square) ![Version](https://img.shields.io/badge/Version-1.2.0-blue?style=flat-square) ![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square) ![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white) ![Stars](https://img.shields.io/github/stars/nikita-liu-ops2096z1/roblox-bunni-launcher-kit?style=flat-square) ![Last Commit](https://img.shields.io/github/last-commit/nikita-liu-ops2096z1/roblox-bunni-launcher-kit?style=flat-square)

Roblox-bunni-launcher — — pixel detection, crosshair overlay, configurable settings

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
 region:
 x1: 100
 y1: 100
 x2: 500
 y2: 400
 target_color: "00FF00"
 threshold: 10

# Hotkeys
hotkeys:
 tool: "F1"
 exit: "F2"

# Monitor
monitor:
 monitor_id: 0 # 0 is usually your primary monitor

# Debugging (WIP)
debug:
 log_level: "INFO" # options: DEBUG, INFO, WARNING, ERROR, CRITICAL
 log_file: "launcher.log"
```

Feel free to edit these values. Restart the app to apply changes.

### Highlights

* **Screen analysis:** Analyzes a specific region of your screen.
* **Overlay:** Draws a simple overlay on your screen.
* **Crosshair:** Customizable crosshair for better visibility.
* **Pixel detection:** Detects when a specific color appears within a defined area.
* **Hotkey automation:** Uses hotkeys to start/stop functionality.
* **Configuration:** Settings are stored in a simple YAML file.

### Usage

First, make sure you have Python 3.11+ installed. Then:

1. **Install dependencies:** Open your terminal, navigate to the directory where you extracted the files, and run `pip install -r requirements.txt`.
2. **Run the main script:** Execute `python main.py`.
3. **Adjust settings:** Modify `config.yaml` to suit your needs (see Config section).
4. **Use hotkeys:** Press the configured hotkeys (defined in `config.yaml`) to tool and de the overlay and other features.

### FAQ

<details>
 <summary>Why isn't the overlay showing up?</summary>
 Make sure you have the necessary permissions. Sometimes Windows restricts overlays. Also, double-check your `monitor_id` in the config.
</details>

<details>
 <summary>The pixel detection isn't working. What's wrong?</summary>
 Verify the `region` and `target_color` in your `config.yaml` are correct. Use a color picker tool to get the precise color value. Also, the `threshold` might be too high.
</details>

<details>
 <summary>Can I run this on Linux/macOS?</summary>
 Currently, it's only tested on Windows. But, the core logic *should* work on other platforms with some adjustments to the `monitor.py` and `input_handler.py` files.
</details>

---

⚡ Fast, lightweight, and easy to use