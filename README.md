# Energy Conversion

## Overview

This program asks the user for any random values of energy in kilocalories and fuel burn rate in gallons per hour. The program converts these input variables to their metric units of ergs and liters per second respectively.

---

## Program Information

**Program:** `conversion.c`

**Author:** John Vianney Ssennono

---

## Description

The program prompts the user to enter:

- Energy in kilocalories
- Fuel burn rate in gallons per hour

The entered values are then converted to the following metric units:

- Ergs
- Liters per second

The converted results are displayed in the terminal.

---

## Repository Structure

```text
Conversion/
│
├── conversion.c
└── README.md
```

---

## Language

- C

---

## Input

The program requests the following values from the user:

- Energy (kilocalories)
- Fuel burn rate (gallons per hour)

---

## Output

The program converts and displays:

- Energy in ergs
- Fuel burn rate in liters per second

---

## Constants Used

The program defines constants for performing the unit conversions, including:

- Joules per calorie
- Ergs per joule
- Quarts per liter
- Calories per kilocalorie
- Quarts per gallon

These constants are declared before the program performs the conversions.

---

## How to Compile

```bash
gcc conversion.c -o conversion
```

---

## How to Run

```bash
./conversion
```

---

## Author

John Vianney Ssennono
