# Multi-Sensor IoT System with RFID

## Overview
This project involves developing an IoT-based multi-sensor system using:
- **NUCLEO-H7A3ZI-Q (STM32-based)**
- **PSoC 6 Wi-Fi BT Prototyping Kit (Cypress/Infineon-based)**

The system collects environmental data from sensors, stores it locally on an SD card, and transmits it via Wi-Fi/Bluetooth to a **MongoDB database**. The data is then visualized using a **Device Monitor**.

---
## Features
- **Real-time sensor data acquisition** (Temperature, Audio, Touch, RFID, etc.)
- **Data logging on SD card & NOR Flash**
- **Wireless communication via Wi-Fi/Bluetooth**
- **RFID authentication system**
- **MongoDB integration for cloud storage**
- **Qt-based Windows application for visualization**
- **Configurable threshold alerts and notifications**
- **Historical data analysis and trend visualization**

---
## Project Milestones

### **Phase 1: Hardware Setup & Sensor Integration** (2-3 weeks)
1. **NUCLEO-H7A3ZI-Q**
   - Configure **SPI** for RFID module
   - Configure **I2C** for OLED Display
   - Implement **ADC** for Thermistor readings
   - Implement **PDM microphones** for audio capture
   - Enable **SD card storage** (FATFS)
   - Implement **GPIO-based touch sensing**
   
2. **PSoC 6 Wi-Fi BT Kit**
   - Configure **CapSense (capacitive touch)**
   - Implement **Wi-Fi/BLE connectivity**
   - Integrate **Quad-SPI NOR Flash**
   - Implement **RFID authentication system**
   - Establish basic UI controls using touch gestures
   
---
### **Phase 2: Communication & Cloud Integration** (3-4 weeks)
- Set up **MongoDB database** for data storage
- Implement **MQTT/WebSockets** for cloud data transfer
- Enable **Wi-Fi/Bluetooth communication** on both boards
- Implement **error handling & retries** for data transmission
- Ensure **real-time data syncing** between edge devices and cloud

---
### **Phase 3: Windows Application with Qt** (4-5 weeks)
- Develop **Qt-based dashboard** to display sensor data
- Implement **data visualization** (graphs, tables, logs)
- Enable **real-time updates** from MongoDB
- Implement **RFID-based authentication UI**
- Add **configurable threshold alerts** (e.g., temperature warnings)
- Implement **exporting data to CSV or JSON for reports**
- Introduce **basic analytics for historical trends**

---
## Testing & Validation Plan

### **Unit Testing (Per Sensor & Module)**
✅ RFID authentication: Validate card scanning and UID retrieval.  
✅ Temperature readings: Verify ADC accuracy against a reference thermometer.  
✅ Audio processing: Test microphone input and PDM-to-PCM conversion.  
✅ Capacitive Touch: Validate user input recognition.  
✅ Data logging: Ensure SD card and NOR Flash store and retrieve data correctly.
✅ Wi-Fi/Bluetooth: Ensure proper connection to network and correct data transmission.

### **Integration Testing**
✅ Sensor data transmission over Wi-Fi/BLE to MongoDB.  
✅ Consistency between logged data (SD card) and cloud data.  
✅ Seamless visualization of data in the Qt application.  
✅ Authentication flow with RFID validation and secure access.

### **Final Validation**
✅ Stress test with multiple RFID scans and continuous data logging.  
✅ Performance testing for real-time updates in Qt UI.  
✅ Ensure power efficiency and optimize for embedded constraints.
✅ Simulate network failures to test fail-safe mechanisms.

---
## Tools & Technologies
- **Embedded Development:** STM32CubeIDE, ModusToolbox
- **Networking:** MQTT, WebSockets, REST API
- **Cloud Storage:** MongoDB, Firebase (optional backup)
- **GUI Development:** Qt for Windows, QML for UI design
- **Data Processing:** Python scripts for data analysis
- **Version Control:** Git/GitHub
- **Testing Tools:** Wireshark for network debugging, J-Flash for firmware validation

---
## Future Enhancements
- **Machine Learning for anomaly detection** (e.g., detecting unusual temperature fluctuations)
- **Mobile application for remote monitoring** (using Flutter or React Native)
- **Battery optimization for long-term IoT deployment**
- **Integration with voice assistants (Alexa, Google Assistant)**
- **Automated reports generation and email notifications**

---
## Contributors
- **Zhanbota Bissaliyeva**  
- **Newton Kelvin**


---
## License
This project is open-source under the **MIT License**.
