<div align="center"><a name="readme-top"></a>
<img src="assets/logo.png"/>

# Auto-Irrigation System for ESP32 🌱💧

<div/>
<div align="left">

This project is an automated irrigation system powered by an ESP32 
microcontroller.<br/>
It uses sensors to monitor soil moisture and water levels, controls a pump for irrigation, and logs information on an LCD display.<br/>
The system ensures efficient water usage while minimizing human intervention.<br/>

## 🌟 Features
- **Soil & Water Monitoring**: Reads data from moisture and water level sensors.
- **Automated Irrigation**: Activates the pump when moisture levels drop below a threshold.
- **LCD Display**: Displays real-time sensor readings and warnings.
- **Wi-Fi Connectivity**: Uses NTP for time synchronization and potential remote monitoring.
- **Energy Efficiency**: Enters deep sleep mode between irrigation cycles.
- **Error Handling**: Provides warnings for low water levels and device initialization failures.

## 🛠️ Hardware Requirements
- ESP32 Development Board
- Soil Moisture Sensor
- Water Level Sensor
- 16x2 LCD with I2C Interface
- Water Pump 5V
- Power Supply (e.g., battery or solar panel)

## 🚀 Getting Started

### 1️⃣ Installation
1. Clone the repository:
```bash
  git clone https://github.com/mistersomov/IoT-AutoIrrigation
```
2. Install `ESP-IDF` (`Espressif IoT Development Framework`):
If you do not have the `ESP-IDF` Framework pre-installed, follow the installation instructions on the official documentation
    [ESP-IDF Get Started](https://docs.espressif.com/projects/esp-idf/en/v5.3.1/esp32/get-started/index.html#installation).
Otherwise skip this step.

3. Configure Wi-Fi credentials:
While in the root directory of the project, execute the command:
```bash
    idf.py menuconfig
```
- Next, `Irrigation Configutraion` menu.
- Go to `Wi-Fi`.
- Enter your credentials.
- Exit with save.

Example:
<div align="center">
<img src="assets/wifi_creds.gif" width="600"/>
</div>

### 2️⃣ Build
After completing the “Installation” item, to build the project, run the command:
```bash
    idf.py -p PORT flash monitor
```
Replace `PORT` with your ESP32 board's USB port name. If the `PORT` is not defined, the `idf.py` will try to connect automatically using the available USB ports.

## 📅 Future Enhancements
- Integration with cloud platforms for remote monitoring.
- Advanced scheduling based on weather data.
- Customizable thresholds via a web interface.

## 📷 Screenshots
<div align="center">
<img src="assets/auto_irrigation.jpg" width="50%" height="50%"/>
</div>
</div>
