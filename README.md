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

## 适配的相关项目

- [MeshCore-TinyLora](https://github.com/Mymetu/MeshCore-TinyLora)
- [mv-game-meshtastic](https://github.com/Mymetu/mv-game-meshtastic)

## 固件烧录方法

1. Chrome / Edge 浏览器打开 `https://wiki.openrtu.run/flash`
2. 从互联网获取设备兼容固件
3. 网页上点击上传固件
4. 连接设备（特殊情况下需要按住 BOOT 按钮再插 USB）
5. 点击连接设备
6. 点击烧录
7. 完成后断开连接