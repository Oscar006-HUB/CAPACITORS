This project uses an ESP32 to read the voltage across a charging or discharging capacitor through its analog input (ADC). By measuring the voltage over time, it enables simple RC circuit analysis, educational demonstrations, or basic capacitive sensing.

Microcontroller: ESP32
Pin Used: GPIO 32 (ADC1 channel)
Reads: Analog voltage (0–3.3V) → converted to 0–4095 (12-bit)
Output: Serial monitor print at 115200 baud
Delay: 200ms between readings

- The capacitor charges through the resistor when 3.3V is applied.
- To **reset**, briefly short the capacitor’s positive lead to GND (manually or via a control pin).
- Use **GPIO32** (or any ADC1-capable pin: 32–39).

> 🔥 **Warning**: Do not apply voltage > 3.3V to ESP32 pins — it may cause permanent damage.

---

## 💻 Code Usage

### 1. Upload the Sketch
- Open in Arduino IDE or PlatformIO.
- Select correct ESP32 board and port.
- Upload `capacitor_reader.ino`.

### 2. View Output
- Open **Serial Monitor** (`Ctrl+Shift+M`)
- Set baud rate to **115200**
- Observe real-time voltage readings

### 3. Key Code Snippet
```cpp
const int capPin = 32; // ADC pin connected to capacitor

void setup() {
  Serial.begin(115200);
}

void loop() {
  int capValue = analogRead(capPin);
  Serial.print("Capacitor Voltage Reading: ");
  Serial.println(capValue);
  delay(200); // Sample every 200ms
}
