# Arduino LCD Contrast Controller with Serial Commands

This project demonstrates how to control the contrast of a 16x2 LCD using an Arduino and serial communication. A simple serial interface lets you adjust the display contrast by sending characters via the Serial Monitor.

## 🛠️ Components Used

- Arduino Uno
- 16x2 LCD Display
- 220-ohm resistor (optional, for backlight current limiting)
- Jumper Wires
- Breadboard

## 🧰 Wiring Overview

The LCD is connected using the 6-pin setup of the `LiquidCrystal` library:

| LCD Pin | Arduino Pin |
|---------|-------------|
| RS      | 12          |
| E       | 11          |
| D4      | 5           |
| D5      | 4           |
| D6      | 3           |
| D7      | 2           |
| VSS     | GND         |
| VDD     | 5V          |
| V0      | PWM pin 6 (Contrast Control) |
| RW      | GND         |
| A (LED+) | 5V         |
| K (LED-) | GND         |

## 💻 How It Works

- Displays a welcome message on startup.
- Uses `analogWrite()` on pin 6 to control the LCD contrast.
- Serial commands:
  - Send `A` to **increase** contrast.
  - Send `B` to **decrease** contrast.
- Continuously shows the time in seconds since the Arduino started.

## 📸 Circuit Diagram

![Arduino LCD_bb](https://github.com/user-attachments/assets/9f46ce3b-3064-43b8-a270-5ec3479f3142)


## 🧪 Getting Started

1. Open the `_8.ino` file in the Arduino IDE.
2. Select your board and port.
3. Upload the sketch.
4. Open the Serial Monitor (9600 baud).
5. Try sending `A` and `B` to control the contrast.


