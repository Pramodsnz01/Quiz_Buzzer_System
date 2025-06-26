# 🧠 8-Channel Quiz Buzzer System using 8051 Microcontroller

This project implements a simple **8-channel quiz buzzer system** using an **8051 microcontroller**, designed to detect the first participant to press the buzzer. The project was developed in **three versions** — simulated in **Proteus + Keil**, and then implemented in real hardware by burning the final version into the microcontroller.

---

## 🔧 Features

- Supports **8 individual channels (participants)**
- Displays the **first pressed button** on a 7-segment display
- Sounds a **buzzer** on detection
- Requires a **reset** button to clear the display and continue
- Works both in **simulation** (Proteus + Keil) and in **real-world hardware**

---

## 🛠️ Hardware Components

- 8051 Microcontroller (AT89C51/AT89S52)
- 8 Push Buttons (for participants)
- 7-Segment Display (Common Cathode)
- Buzzer
- Resistors, Breadboard, Wires
- Optional: Crystal Oscillator, Capacitors (for clock)

---

## 💻 Software Used

- **Keil uVision** (for coding & simulation)
- **Proteus** (for circuit simulation)
- **8051 Programmer** (for burning .hex to microcontroller)

---

## ⚙️ How It Works

1. The system waits until **one of the 8 buttons is pressed**.
2. Once a button is pressed:
   - The **corresponding number (1–8)** is shown on the 7-segment display.
   - The **buzzer sounds** for a short duration.
   - **All other inputs are disabled** until the system is reset.
3. The system only proceeds when the **reset button is pressed**.

---

## 🧪 Code Versions

| Version | File Name    | Description                              |
|---------|--------------|------------------------------------------|
| V1      | `quizzz.c`   | First version with core logic separation, modular `display()` and `buzzer()` functions |
| V2      | `Quizz.c`    | Mid version, full integration in `main()`, added resets and improved layout |
| V3      | `Quiz.c`     | Final version tested and flashed to hardware |

> ✅ The final version (`Quiz.c`) was verified on a **real 8051 microcontroller board**.

---

## 🧰 Pin Configuration

| Port | Purpose                        |
|------|--------------------------------|
| P1   | Input buttons (SW1 to SW8)     |
| P2   | 7-Segment display control      |
| P3.0 | Buzzer output                  |
| P3.1 | Stop/reset button (V1 only)    |
| P3.3 | Reset switch (V2 & V3)         |
| P3.7 | 7-Segment display enable pin   |
| P0.0 | Buzzer output (V1 only)        |

---

## 🚀 Getting Started (Simulation)

1. Open `Quiz.c` or `Quizz.c` in **Keil** and compile to generate `.hex`.
2. Open **Proteus**, create the circuit and import `.hex` into the 8051 IC.
3. Run simulation and test each button.
4. Ensure buzzer and display behave as expected.

---

## 🔥 Flashing to Microcontroller

1. Use any 8051 USB Programmer.
2. Flash the `.hex` file from `Quiz.c`.
3. Wire up the buttons, display, and buzzer as per the circuit.
4. Power the system and test it live.

---

## 🙌 Author

**Pramod Singh**  
Electronics Enthusiast | Embedded Developer  
[LinkedIn](https://www.https://www.linkedin.com/in/pramodsnz/) | [GitHub](https://https://github.com/Pramodsnz01)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

