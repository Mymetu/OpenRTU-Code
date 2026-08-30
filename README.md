# OpenRTU-Code

TinyLora 系列 LoRa 系列开发板固件与资源仓库。

## 项目简介

OpenRTU-Code 是围绕 **TinyLora 系列** 低功耗 LoRa 自组网设备整理的固件与配套资源仓库，覆盖多款基于 ESP32 的板卡，支持 MeshCore / Meshtastic 等固件的编译与刷机。

## 支持的板卡

| 板卡 | 主控 | LoRa 射频 | 说明 |
|---|---|---|---|
| TinyLora C3 V2 (22S/29S) | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | E22-900M 系列模块，29S 带 PA |
| TinyLora C3 V3 (22S/29S) | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 可选 AHT20+BMP280 传感器 |
| TinyLora C3 V3 GPS | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 带 GPS（Serial1） |
| TinyLora C3 V4/V5 | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | LED 心跳指示 |
| TinyLora C6 | ESP32-C6 | LoRa | WS2812 彩灯、蜂鸣器、外部看门狗、GPS |
| TinyLora MV ZHCN | ESP32-C3 | SX1262 | GPS + 环境传感器（AHT20+BMP280） |

## 固件支持

- **MeshCore**：轻量级多跳 LoRa 组网协议库（MIT License）
- **Meshtastic**：TinyLora 部分型号可刷 Meshtastic 固件

每个板卡通常提供两种固件形态：

- `repeater`：中继节点
- `companion_radio_ble`：搭配手机客户端使用

## 特性

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
