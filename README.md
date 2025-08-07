# 🚗 Arduino Robot Car (Bluetooth + L298N)

Autonomous/remote-controlled robot car using Arduino, L298N motor driver, and HC-05 Bluetooth modules.

---

## 🛠 Components
- Arduino Uno (car) + Arduino Nano (joystick)  
- L298N dual motor driver  
- 12V DC gear motors (x2)  
- HC-05 Bluetooth: **Master** (joystick) ↔ **Slave** (car)  
- Joystick module  
- 3× 18650 Li-ion (≈11.1 V) battery pack  
- Level divider (1 kΩ & 2 kΩ) for HC-05 TX→RX  
- Wires, chassis, wheels

---

## 📂 Files
- `robot_car.ino` — car/slave firmware  
- `rc-remote-control-car.png` — wiring diagram

---

## 📷 Circuit Diagram
![Circuit diagram](rc-remote-control-car.png)

---

## ▶ How to Run
1. Wire everything per the diagram.  
2. Upload `robot_car.ino` to the **car** Arduino.  
3. Configure HC-05 roles (one **Master**, one **Slave**) and pair them.  
4. Power the car with the 3×18650 pack.  
5. Control the car with the joystick via Bluetooth.

---

## ⚠️ Notes
- L298N **12V** to motor supply; share **GND** with Arduino.  
- Use a voltage divider on Arduino TX → HC-05 RX (5 V → ~3.3 V).  
- If motors brown-out the Arduino, power logic separately (with common GND).

---

## 📜 License
MIT
