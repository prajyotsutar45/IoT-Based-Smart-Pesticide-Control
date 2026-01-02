# Smart Infection-Risk Aware Water & Pesticide Spraying Robot

## Team Details
- **Team Name:** Shockwave Squad  
- **College:** D.Y. Patil School of Engineering & Management (DYPSEM)  
- **Hackathon:** Dimension X Hackathon  

---

## Project Overview
Farmers often spray pesticides based on experience or fixed schedules, which leads to chemical overuse, health risks, and environmental damage.  
This project presents a **farmer-assisted robotic system** that helps reduce unnecessary pesticide spraying using sensors and vision-based risk indication.

The system **does not replace the farmer**.  
It provides real-time risk indicators, while the final spraying decision remains manual for safety and reliability.

---

## Key Features
- Mobile robot for farm-row movement  
- Sensor-based infection risk estimation  
- Vision-assisted leaf stress detection  
- LED-based risk indication  
- Manual control for water and pesticide spraying  
- Low-cost and scalable design  

---

## System Architecture
The system is divided into three independent modules:

1. **Robot Control Unit (ESP NodeMCU #1)**
   - Controls robot movement
   - Handles obstacle detection

2. **Spray & Decision Unit (ESP NodeMCU #2)**
   - Reads environmental and soil sensors
   - Receives stress value from ESP32-CAM
   - Indicates risk level using LEDs
   - Controls water and pesticide pumps

3. **Vision Module (ESP32-CAM)**
   - Captures leaf images
   - Performs simple pixel-based analysis
   - Converts image into a numeric stress value
   - Sends stress value wirelessly via Wi-Fi

---

## Working Principle
1. Robot moves manually in the field  
2. Robot stops near a plant  
3. ESP32-CAM captures leaf image  
4. Visual stress value is calculated  
5. Sensor data is combined with stress value  
6. LEDs indicate infection risk level  
7. Farmer manually triggers water or pesticide spray  

---

## ESP32-CAM Working
- Operates as a **standalone vision module**
- Powered independently (5V & GND only)
- No data wires connected to NodeMCU
- Sends only a **numeric stress value**, not raw images
- Communication via Wi-Fi (HTTP request)

> The ESP32-CAM provides visual assistance, not medical disease diagnosis.

---

## Auto & Manual Control Logic
| Function | System (Auto) | Farmer (Manual) |
|--------|---------------|-----------------|
| Risk calculation | ✔ | — |
| LED indication | ✔ | — |
| Water spray | — | ✔ |
| Pesticide spray | — | ✔ |
| Final decision | — | ✔ |

---

## Hardware Components
- ESP8266 NodeMCU (2 units)
- ESP32-CAM (AI Thinker)
- L298N Motor Driver
- DC Motors & Robot Chassis
- Ultrasonic Sensor
- DHT11 / DHT22 Sensor
- Capacitive Soil Moisture Sensor
- Dual Channel Relay Module
- Water Pump
- Pesticide Pump
- LEDs, Buzzer, Push Buttons
- Power Supply & Wiring

---

## Cost Estimation
- **Prototype Cost:** ₹2,600 – ₹3,000  
- Cost can be reduced in bulk production  
- Designed to be affordable for small and medium farmers  

---

## Advantages
- Reduces unnecessary pesticide usage  
- Improves farmer safety  
- Environment-friendly  
- Simple and reliable operation  
- Modular and scalable design  

---

## Limitations
- Cannot heal already damaged leaves  
- Requires crop-specific calibration  
- Camera performance depends on lighting conditions  

---

## Future Scope
- AI-based disease classification  
- Mobile application integration  
- Solar-powered operation  
- Fully autonomous spraying mode  

---

## Conclusion
This project demonstrates a **practical and farmer-centric approach** to smart agriculture by combining robotics, sensors, and vision assistance.  
By keeping the farmer in control, the system ensures safety while promoting efficient and responsible pesticide usage.

> **The system thinks automatically, but the farmer always decides.**
