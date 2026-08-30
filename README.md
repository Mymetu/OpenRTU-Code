# OpenRTU-Code

OpenRTU 项目固件与资源仓库。

## TinyLora 系列

低功耗 LoRa 开发板系列，基于 ESP32，支持 MeshCore / Meshtastic 固件。

### 支持的板卡

| 板卡 | 主控 | LoRa 射频 | 说明 |
|---|---|---|---|
| TinyLora C3 V2 (22S/29S) | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 255MN-L03、RA-01SC/RA-01SC-P、RA-01S/RA-01S-P、HT-RA62、255MN-L08、E22-900M 系列，29S 带 PA |
| TinyLora C3 V3 (22S/29S) | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 255MN-L03、RA-01SC/RA-01SC-P、RA-01S/RA-01S-P、HT-RA62、255MN-L08，可选 AHT20+BMP280 |
| TinyLora C3 V3 GPS | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 255MN-L03、RA-01SC/RA-01SC-P、RA-01S/RA-01S-P、HT-RA62、255MN-L08，带 GPS（Serial1） |
| TinyLora C3 V4/V5 | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 E220-400M30S、E22-400M30S、E22-400M33S、E220-900M30S、E22-900M30S、E22-900M33S，LED 心跳指示 |
| TinyLora MV ZHCN | ESP32-C3 | SX1262 | GPS + 环境传感器（AHT20+BMP280） |

### 固件形态

每个板卡通常提供两种固件：

- `repeater` — 中继节点
- `companion_radio_ble` — 搭配手机客户端使用

### 固件支持

- **MeshCore**：轻量级多跳 LoRa 组网协议库（MIT License）
- **Meshtastic**：部分型号可刷 Meshtastic 固件

### 特性

- LoRa 射频芯片运行时自动识别（SX1262 / SX1268 / LLCC68）
- 默认频率 480.375MHz、SF9、125kHz 带宽
- ESP-IDF 动态调频 + light sleep 低功耗
- 锂电池电压检测

## 快速开始

### 环境要求

- [PlatformIO](https://platformio.org)（VS Code 插件）
- Git

### 编译

以 TinyLora C3 V4/V5 中继为例：

```bash
git clone https://github.com/Mymetu/OpenRTU-Code.git
cd OpenRTU-Code
pio run -e TinyLora_C3_V4_V5_repeater
```

### 刷机

编译完成后在 `.pio/build/<目标>/` 目录下生成固件，可用 esptool 或 [esptool-js 网页工具](https://espressif.github.io/esptool-js/) 烧录。

## 目录结构

```
OpenRTU-Code/
├── boards/         # 板卡定义
├── variants/       # 各板卡引脚与平台配置
├── src/            # 固件源码
└── docs/           # 文档
```

## 相关项目

- [MeshCore](https://github.com/ripplebiz/MeshCore)

## 许可证

本仓库内固件遵循各自上游项目的开源许可证（MeshCore 为 MIT License）。