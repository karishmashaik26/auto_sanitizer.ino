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

1. IR sensor detects hand at close range (typically gives a LOW signal).
2. Arduino activates:
   - **LED** as visual indicator
   - **Relay/Motor** to pump sanitizer
3. When the hand is removed:
   - Both LED and pump turn OFF

---

## 💾 Arduino Code

```cpp
int IRsensor = 2;         // IR sensor input pin
int LED = 12;             // LED output pin
int SANITIZER = 11;       // Pump/relay output pin

void setup() {
  pinMode(IRsensor, INPUT);
  pinMode(LED, OUTPUT);
  pinMode(SANITIZER, OUTPUT);
}

void loop() {
  int statusSensor = digitalRead(IRsensor);

  if (statusSensor == 0) {              // Hand detected
    digitalWrite(LED, HIGH);           // Turn on LED
    digitalWrite(SANITIZER, HIGH);     // Activate pump
  } else {
    digitalWrite(LED, LOW);            // Turn off LED
    digitalWrite(SANITIZER, LOW);      // Deactivate pump
  }
}


