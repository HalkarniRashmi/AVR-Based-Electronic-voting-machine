# 🗳️ Electronic Voting Machine using AVR Microcontroller

This project implements a **basic electronic voting machine (EVM)** using an **AVR microcontroller** (e.g., ATmega16/32). The system allows users to cast votes for one of four political parties using push buttons and view the results on an LCD display.

## ✅ Features

- Voting for **4 political parties**:
  - 🟠 BJP  
  - 🟦 INC  
  - 🟣 AAP  
  - 🟢 TMC  
- **Result button** to display vote counts.
- **16x2 LCD** used for displaying messages and results.
- **Debounce logic** ensures one vote per button press.
- Uses **internal pull-up resistors** to avoid floating inputs.
- LCD operates in **4-bit mode** to reduce pin usage.

---

## 🧠 Working Principle

- Each party is assigned a push button.
- On pressing a party’s button:
  - The corresponding vote count is incremented.
  - A confirmation message (e.g., “Vote Casted for BJP”) is shown on the LCD.
- Pressing the **"Result"** button:
  - Displays total votes for each party one by one on the LCD screen.

---

## 🔧 Hardware Configuration

| Component           | Description                                |
|---------------------|--------------------------------------------|
| Microcontroller     | ATmega16 / ATmega32                        |
| LCD                 | 16x2 Character LCD (in 4-bit mode)         |
| Buttons             | 5 push buttons (BJP, INC, AAP, TMC, Result)|
| Pull-up Resistors   | Internal pull-ups used on button inputs    |
| Power Supply        | 5V regulated                               |

---

## 📟 LCD Pin Mapping

| LCD Pin | AVR Port | Notes          |
|---------|----------|----------------|
| RS      | PORTC    | Control Signal |
| E       | PORTC    | Control Signal |
| D4–D7   | PORTD    | Data Lines     |

---

## 📁 Files Included

- `main.c` – Main source file with logic for voting and LCD display.
- `lcd.h` / `lcd.c` – LCD 4-bit mode driver.
- `Makefile` – For compilation and uploading via AVRDUDE (optional).

---

## 🚀 Future Improvements

- Add password-protected result access.
- Include buzzer feedback on vote cast.
- Use EEPROM to store vote counts across resets.
- Support graphical LCD or OLED for better UI.

---


