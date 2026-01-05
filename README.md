# duino-coin-esp32-c3
Version for esp32-c3 super mini amoled 044inch . 

> **Minor source code modifications to support the built-in 0.44" AMOLED display (72x64) on ESP32-C3 Super Mini, showing basic mining statistics in real-time.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/Platform-ESP32--C3-blue.svg)](https://www.espressif.com/en/products/socs/esp32-c3)
[![Duino-Coin](https://img.shields.io/badge/Duino--Coin-v4.3-green.svg)](https://duinocoin.com)

## Demo

<table>
<tr>
<td width="50%">
<img src="https://github.com/Mytai20100/duino-coin-esp32-c3/blob/main/img/esp32-c3-mining-1-4-2026-github1.png" alt="nọting" width="100%">
</td>
<td width="50%">

### Display

The screen shows:
- **Accepted/Total shares**
- **Node name** and **ping**
- **Difficulty** level


My camera is bad ;ccc

</td>
</tr>
<tr>
<td width="50%">
<img src="https://github.com/Mytai20100/duino-coin-esp32-c3/blob/main/img/esp32-c3-mining-1-4-2026-github2.png" alt="Hardware Setup" width="100%">
</td>
<td width="50%">

### ???

????



</td>
</tr>
</table>

---

## Features
- **Display Support**: Real-time mining stats on built-in 0.44" AMOLED display
## Performance

| Device | Hashrate | Power |
|--------|----------|-------|
| ESP32-C3 @ 240MHz | ~62-64 kH/s | ~0.6W |

### Display Pinout (Built-in)
- **SDA**: GPIO 5
- **SCL**: GPIO 6
- **Resolution**: 72x40 pixels
- **Driver**: SSD1306 compatible

## Installation

### 1. Install Arduino IDE & Libraries

Install the following libraries via **Library Manager**:
- `ArduinoJson` by Benoit Blanchon
- `U8g2` by oliver (for OLED display)

### 2. Configure Arduino IDE

**Board Settings:**
```
Board: "ESP32C3 Dev Module"
Upload Speed: 921600
CPU Frequency: 240MHz (WiFi)
Flash Size: 4MB
Partition Scheme: Default 4MB with spiffs
```

### 3. Update Settings

Edit `Settings.h`:

```cpp
// ---------------------- General settings ---------------------- //
// Change the part in brackets to your Duino-Coin username
extern char *DUCO_USER = "";
// Change the part in brackets to your mining key (if you have set it in the wallet)
extern char *MINER_KEY = "";
// Change the part in brackets if you want to set a custom miner name
// Use Auto to autogenerate, None for no custom identifier
extern char *RIG_IDENTIFIER = "none";
// Change the part in brackets to your WiFi name
extern const char SSID[] = "yourwifi";
// Change the part in brackets to your WiFi password
extern const char PASSWORD[] = "your password wifi";
```

### 4. Upload

1. Connect ESP32-C3 via USB-C
2. Select correct COM port
3. Click **Upload**

### OLED Display
The screen shows stats:
```
┌──────────────┐
│ 25/26        │  ← Shares (accepted/total)
│ Node-1 45ms  │  ← Node name + ping
│ D:150        │  ← Difficulty
└──────────────┘
```

## Advanced Configuration

### Overclocking
Current setting: **240MHz** (in `ESP_Code.ino`)

Try higher frequencies (at your own risk):
```cpp
setCpuFrequencyMhz(280);  // Experimental
```

## Changes from Original

This fork includes:
- Modified `DisplayHal.h` for 72x40 AMOLED support
- Updated `Settings.h` with correct I2C pins (GPIO5/6)
- Optimized display layout for small screen
- Pre-configured for ESP32-C3 Super Mini

## Credit

- **Original Duino-Coin**: [github.com/duino-coin/duino-coin](https://github.com/duino-coin/duino-coin)
- **Duino-Coin Website**: [duinocoin.com](https://duinocoin.com)
- **ESP32-C3 Datasheet**: [Espressif](https://www.espressif.com/en/products/socs/esp32-c3)
- **U8g2 Library**: [github.com/olikraus/u8g2](https://github.com/olikraus/u8g2)

## License

MIT License - Based on [Duino-Coin](https://github.com/duino-coin/duino-coin?tab=MIT-1-ov-file) project

**The Duino-Coin Team & Community © 2019-2026**

**Made for the Duino-Coin community**

*Happy Mining! :3*
