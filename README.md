# Smart-Industrial-Process-monitoring-system-using-IOT-V24HE4S16
This project aims to develop an industrial process monitoring system using IOT, featuring sensors(LM35 for temperature and MQ-2 for gas/smoke) interfaced with LPC2148 microcontroller. Data is displayed on the LCD and sent to ThingSpeak cloud via an ESP01 Wi-Fi module for real-time monitoring and alerts.  

## 🚀 Features

- 📡 Real-time monitoring of industrial parameters (temperature, gas, etc.)
- 📲 Wireless data transmission using Wi-Fi (ESP01/LPC2148)
- 🔔 Alert notifications on abnormal conditions
- 💾 Data logging and visualization via cloud platforms (e.g., ThingSpeak)
- ⚙️ Easy integration with industrial systems

## 🧰 Components Used

- **Microcontroller:** LPC2148 (ESP01)
- **Sensors:**
  - MQ-2 (Gas/Smoke sensor)
  - LM35 (Temperature & Humidity sensor)
- **IoT Platform:** ThingSpeak (or any compatible platform)
- **Other:**
  - Power supply
  - Breadboard and jump wires

## 🔧 How It Works

1. Sensors collect real-time data from the environment.
2. The microcontroller processes the sensor data.
3. Data is transmitted via Wi-Fi to the IoT platform.
4. Users can view data on the dashboard and receive alerts if thresholds are breached.

## 🛠️ Setup Instructions

### 1. Hardware Setup:
- Connect sensors to LPC2148 as per the circuit diagram.
- Ensure proper power supply and stable Wi-Fi connectivity.

### 2. Software Setup:
- Use **Arduino IDE** for programming the ESP8266 (ESP-01).
- Select the appropriate board: `Generic ESP8266 Module`.
- Install the required libraries:
  - `ESP8266WiFi` – for WiFi connectivity
  - `ThingSpeak` – for cloud data logging
- Connect the LM35 sensor output to the **ADC (A0)** pin of ESP-01 (use a voltage divider if necessary, as ESP-01 ADC max input is 1V).
- Modify the code to read analog values from A0 and convert them to temperature using the LM35 formula: Temperature (°C) = (analogRead(A0) * 3.3 / 1023) * 100

### 3. Cloud Configuration:
- Create a ThingSpeak channel.
- Add fields for each sensor value.
- Get the API key and add it in the code.


