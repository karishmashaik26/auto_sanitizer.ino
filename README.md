# auto_sanitizer.ino
# ✋ Automatic Hand Sanitizer Dispenser using IR Sensor – Arduino

This Arduino project activates a **sanitizer pump** automatically when a hand is detected using an **IR proximity sensor**. It also turns on an **LED indicator** during dispensing.

---

## 🧰 Components Required

- Arduino UNO  
- IR Sensor Module  
- LED  
- Relay Module or small DC pump  
- 12V Motor (optional)  
- Jumper wires, Breadboard

---

## 🔌 Pin Configuration

| Component   | Arduino Pin |
|-------------|-------------|
| IR Sensor   | D2          |
| LED         | D12         |
| Pump Relay  | D11         |

---

## 🚦 How It Works

1. IR sensor detects hand at close range (outputs LOW).
2. Arduino activates:
   - **LED** as status indicator
   - **SANITIZER pin** (relay/motor) to pump sanitizer
3. When the hand is removed:
   - Both LED and pump turn OFF

---

## 📂 Files

- `code/auto_sanitizer.ino` – Main Arduino sketch

---

## 💡 Applications

- Touchless hand sanitizing stations  
- School or office safety systems  
- Covid-19 prevention measures  
- Smart hygiene projects


