# duino-coin-esp32-c3
Version for esp32-c3 super mini amoled 044inch . Hmm 

> **Minimal project custom to support the built-in 0.44" AMOLED display (72x64) on ESP32-C3 Super Mini**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/duino-coin/duino-coin?tab=MIT-1-ov-file)
[![Platform](https://img.shields.io/badge/Platform-ESP32--C3-blue.svg)](https://www.espressif.com/en/products/socs/esp32-c3)
[![Duino-Coin](https://img.shields.io/badge/Duino--Coin-v4.3-green.svg)](https://duinocoin.com)
![Mining](https://img.shields.io/badge/Mining-ESP32--C3-orange)
![Updated](https://img.shields.io/github/last-commit/Mytai20100/duino-coin-esp32-c3)
![Alive](https://img.shields.io/badge/Project-Not_Dead-green)
## Demo

<table>
<tr>
<td width="50%">
<img src="https://github.com/Mytai20100/duino-coin-esp32-c3/blob/main/img/esp32-c3-mining-1-4-2026-github1.png" alt="nọting" width="100%">
</td>
<td width="50%">

### Display
**1/4/2026**
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
**1/4/2026**
????



</td>
</tr>
</table>

---
### Update **1/5/2026**
<table>
<tr>
<td width="50%">
<img src="https://github.com/Mytai20100/duino-coin-esp32-c3/blob/main/img/esp32-c3-mining-1-5-2026-github5.png" alt="nọting" width="100%">
</td>
<td width="50%">

### Boot screen
**1/5/2026**




</td>
</tr>

<tr>
<td width="50%">
<img src="https://github.com/Mytai20100/duino-coin-esp32-c3/blob/main/img/esp32-c3-mining-1-5-2026-github4.png" alt="Detect node" width="100%">
</td>
<td width="50%">

### Detect node
**1/5/2026**
nothing



</td>
</tr>
<tr>
<td width="50%">
<img src="https://github.com/Mytai20100/duino-coin-esp32-c3/blob/main/img/esp32-c3-mining-1-5-2026-github6.png" alt="Detect node" width="100%">
</td>
<td width="50%">

### Connect node
**1/5/2026**
nothing



</td>
</tr>

<tr>
<td width="50%">
<img src="https://github.com/Mytai20100/duino-coin-esp32-c3/blob/main/img/esp32-c3-mining-1-5-2026-github3.png" alt="Detect node" width="100%">
</td>
<td width="50%">

### Stats mining
**1/5/2026**
nothing



</td>
</tr>
</table>

---
## Esp32-c3 super mini 
<img src="https://raw.githubusercontent.com/Mytai20100/duino-coin-esp32-c3/main/img/esp32-c3-u.png"
     alt="ESP32-C3 U"
     width="400"></img>
 <img src="https://raw.githubusercontent.com/Mytai20100/duino-coin-esp32-c3/main/img/esp32-c3-i.png"
     alt="ESP32-C3 U"
     width="400"></img>
## Features
- **Display Support**: Real-time mining stats on built-in 0.44" AMOLED display
## Performance

| Device | Hashrate | Power |
|--------|----------|-------|
| ESP32-C3 @ 240MHz | ~62-64.7 kH/s | ~0.6W |

### Display Pinout (Built-in)
- **SDA**: GPIO 5
- **SCL**: GPIO 6
- **Resolution**: 72x64 pixels
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
```
┌──────────────┐
|    63.7kh/s  |  ← Hash 
│     25/26    │  ← Shares (accepted/total)
│ mc joh-u 67ms│  ← Node name + ping
│     D:1500   │  ← Difficulty
└──────────────┘
```

## Advanced Configuration

### Overclocking
Current setting: **240MHz** (in `ESP_Code.ino`)

Try higher frequencies (at your own risk):
```cpp
setCpuFrequencyMhz(267);  // Experimental
```

## Changes from Original

This fork includes:
- Modified `DisplayHal.h` for 72x64 AMOLED support
- Updated `Settings.h` with correct I2C pins (GPIO5/6)
- Optimized display layout for small screen
- Pre-configured for ESP32-C3 Super Mini
## Where buy it ?
- [Amazon](https://www.amazon.com/ESP32-Development-Supermini-Bluetooth-Type-C/dp/B0FQ487RYT/ref=sr_1_17?crid=1O2DDPV2NKHX5&dib=eyJ2IjoiMSJ9.fkPDLHXqmKvjyoMjtD_a_BklrDI3ilIJ0noj2dSTWgTZ4X_SEWc_jL5oBtoy6gBi7WpwWKQvdtISBctXI8WJN7zQSzQt0Kzj7zZlBIIqdk-xgK3iMQjfs8owxmfqTHUuYT0fwazVjywG_f9JjYxSyFDojW0dl2dkrQrGAWQkF0uv0TM6EurqIw91sga6_oL4NQ-ziN87QL2BaEMn8yZoae2obris82NwpwxU_zGtTZw.v5gba5We7n_oXsF6sJxvXCgOLj_dAGtkCIrzvQavk6c&dib_tag=se&keywords=esp32-c3+super+mini+amoled&qid=1768068111&sprefix=esp32-c3+super+mini+amol%2Caps%2C422&sr=8-17)
- Ebay ? 
## Credit
- **Original Duino-Coin**: [github.com/duino-coin/duino-coin](https://github.com/duino-coin/duino-coin)
- **Duino-Coin Website**: [duinocoin.com](https://duinocoin.com)
## License

MIT License - Based on [Duino-Coin](https://github.com/duino-coin/duino-coin?tab=MIT-1-ov-file) project

**The Duino-Coin Team & Community © 2019-2026**
## Change logs
- *1/4/2026* fork from https://github.com/duino-coin/duino-coin and update somethings -_-
- *1/5/2026* Update Ui remove somthing add #pragma GCC optimize("-funroll-loops"), #pragma GCC optimize("-fprefetch-loop-arrays") in ESP_CODE.ino.
------
**Made for the Duino-Coin community**

*Happy Mining! :3*
