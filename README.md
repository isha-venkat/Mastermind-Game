# Mastermind-Game (Raspberry Pi C + ARM Assembly)
The Raspberry Pi acts as the **codekeeper**, and the player acts as the **codebreaker**, inputting guesses using a button. Feedback is provided through LEDs and an LCD screen.

---

## 🔧 Hardware Requirements

- Raspberry Pi 2, 3, or 4 (not 5)
- Breadboard and jumper wires
- 2 LEDs (Red = control, Green = data)
- 1 Push Button
- 1 16x2 LCD Display with potentiometer
- Power supply (3.3V)
- GPIO Pins used:
  - Red LED → GPIO 5
  - Green LED → GPIO 26
  - Button → GPIO 19
  - LCD Data Pins → GPIO 10, 22, 23, 27

---

## 🛠️ Software Stack

- C (GCC)
- ARM Assembler (for GPIO control and matching logic)
- Raspberry Pi OS (32-bit)
- GNU Toolchain (`gcc`, `as`, `ld`)
- Optional: `gdb`, Address Sanitizer for debugging

---

## 🕹️ Game Features

- Personalized greeting via LED blinks
- Accepts button presses to input guesses
- Red LED = control signals, Green LED = data
- Feedback for each guess:
  - Number of exact matches
  - Number of colour-only matches
- Displays result on LCD
- "SUCCESS" message on correct guess

---

## 💻 Command-Line Options

```bash
./cw2                     # Run full game normally
./cw2 -d                  # Debug mode (show secret, guesses, answers)
./cw2 -s <sequence>       # Manually set secret sequence
./cw2 -u <seq1> <seq2>    # Unit test (compare 2 sequences)
