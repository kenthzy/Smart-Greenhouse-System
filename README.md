# 🌱 Smart Greenhouse System 

IoT-based automated greenhouse using ESP32 for environmental control.

![Greenhouse Model](/assets/images/view-1.png)

## 🌟 Key Features
- 🌡️ Monitors temperature, humidity, soil moisture, and light
- 🌱 Plant hydration check with soil sensor
- 🌊 Automatic watering system
- 🌪️ Climate control with dual fans
- 📱 Remote monitoring via Blynk app
- 📊 Real-time sensor dashboard

## 📦 Components
| Component          | Usage                     |
|--------------------|---------------------------|
| 🎛️ ESP32           | Main controller           |
| 🌡️ DHT22 Sensor    | Temperature/Humidity      |
| 🌿 Soil Moisture   | Plant hydration check     |
| 💦 5V Water Pump   | Automatic watering        |
| 🌬️ 2x 5V Fans     | Temperature regulation    |

## 🔧 Setup Guide
1. 🔌 Wire components as per [circuit diagram](/assets/images/diagram.png)
2. 📚 Install required libraries:
   - Adafruit_Sensor
   - DHT.h
   - Blynk
3. ⬆️ Upload `greenhouse-code.txt` to ESP32

## 🤖 Control Logic
```cpp
// ⚙️ Automation Rules
void controlSystems() {
  if (soilMoisture < 30%) pump.start();  // 💧 Water plants
  if (temperature > 28°C) fan1.start(); // 🌪️ Cool system
}
```
- 💾 [Download Code](/assets/source-code/greenhouse-code.txt)

- 📖 [Instruction Manual](/assets/source-code/Instruction.pdf)
