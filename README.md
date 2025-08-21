This project uses an ESP32 to read the voltage across a charging or discharging capacitor through its analog input (ADC). By measuring the voltage over time, it enables simple RC circuit analysis, educational demonstrations, or basic capacitive sensing.

Microcontroller: ESP32
Pin Used: GPIO 32 (ADC1 channel)
Reads: Analog voltage (0–3.3V) → converted to 0–4095 (12-bit)
Output: Serial monitor print at 115200 baud
Delay: 200ms between readings
