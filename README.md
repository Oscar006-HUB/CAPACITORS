# Capacitor Voltage Reader (ESP32)

Reads the voltage across a charging or discharging capacitor through the ESP32's ADC and prints it over serial, for simple RC circuit analysis and demonstrations.

## Hardware
- ESP32 development board
- Capacitor + resistor (RC circuit), measurement node on GPIO 32

## Usage
1. Open `CAPACITOR.ino` in the Arduino IDE with ESP32 board support installed.
2. Upload, then open the Serial Monitor at **115200 baud**.
3. Readings (0–4095 raw ADC) appear every 200 ms; plot them with the Serial Plotter to see the charge/discharge curve.

## License

Released under the [MIT License](LICENSE).
