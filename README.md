# OpenRTU-Code

OpenRTU 项目固件与资源仓库。

## TinyLora 系列

低功耗 LoRa 开发板系列，基于 ESP32，支持多个开源项目。

### 由于大部分硬件已开源，并且支持多种Lora模组，详情参考下面。

| 板卡                          | 主控       | LoRa 射频                        | 说明                                                                                    |
| --------------------------- | -------- | ------------------------------ | ------------------------------------------------------------------------------------- |
| TinyLora C3 V2 (22S/29S)    | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 255MN-L03、RA-01SC/RA-01SC-P、RA-01S/RA-01S-P、HT-RA62、255MN-L08、E22-900M 系列，29S 带 PA |
| TinyLora C3 V3 (22S/29S)    | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 255MN-L03、RA-01SC/RA-01SC-P、RA-01S/RA-01S-P、HT-RA62、255MN-L08，可选 AHT20+BMP280      |
| TinyLora C3 V3 GPS(22S/29S) | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 255MN-L03、RA-01SC/RA-01SC-P、RA-01S/RA-01S-P、HT-RA62、255MN-L08，带 GPS（Serial1）       |
| TinyLora C3 V4/V5           | ESP32-C3 | SX1262 / SX1268 / LLCC68（自动识别） | 支持 E220-400M30S、E22-400M30S、E22-400M33S、E220-900M30S、E22-900M30S、E22-900M33S，LED 心跳指示 |
| TinyLora MV ZHCN            | ESP32-C3 | SX1262                         | GPS + 环境传感器（AHT20+BMP280）+屏幕+蜂鸣器+WS2812                                               |

## 相关项目

- [MeshCore-TinyLora](https://github.com/Mymetu/MeshCore-TinyLora)
- [mv-game-meshtastic](https://github.com/Mymetu/mv-game-meshtastic)