# NumberSystemConverter

A Java program that converts numbers between binary, octal, decimal,
and hexadecimal with a menu-driven interface.

---

## File

| File | Description |
|---|---|
| `NumberSystemConverter.java` | Single file containing all conversion methods and the menu |

---

## How to Run

**Step 1 — Compile:**
```bash
javac NumberSystemConverter.java
```

**Step 2 — Run:**
```bash
java NumberSystemConverter
```

---

## Menu Options

```
NUMBER SYSTEM CONVERTER
[1]  Decimal      -> Binary, Octal, Hex
[2]  Binary       -> Decimal, Octal, Hex
[3]  Octal        -> Decimal, Binary, Hex
[4]  Hexadecimal  -> Decimal, Binary, Octal
[5]  Run all demo conversions
[0]  Exit
```

---

## Sample Output

```
Choose option: 1
Enter a Decimal number: 255
Converting 255 from Decimal:
  Decimal     :  255
  Binary      :  11111111
  Octal       :  377
  Hexadecimal :  FF

Choose option: 2
Enter a Binary number (e.g. 1101): 1101
Converting 1101 from Binary:
  Decimal     :  13
  Binary      :  1101
  Octal       :  15
  Hexadecimal :  D

Choose option: 5
  Decimal    Binary          Octal      Hexadecimal
  0          0               0          0
  1          1               1          1
  10         1010            12         A
  255        11111111        377        FF
  ...
```

---

## Methods

| Method | Description |
|---|---|
| `toBinary(int n)` | Converts decimal to binary |
| `toOctal(int n)` | Converts decimal to octal |
| `toHex(int n)` | Converts decimal to hexadecimal |
| `fromBinary(String s)` | Converts binary to decimal |
| `fromOctal(String s)` | Converts octal to decimal |
| `fromHex(String s)` | Converts hexadecimal to decimal |
| `showAll(int dec)` | Displays all four conversions from a decimal value |
| `runDemo()` | Prints a table of 20 sample conversions |

---

## How Conversion Works

All conversions go through decimal as the middle step:

- **Input is decimal** → directly converted to the other three bases
- **Input is binary / octal / hex** → first converted to decimal, then to the remaining two bases

Conversions are done manually using division and remainder loops — no built-in methods like `Integer.toBinaryString()` are used.

---

## Error Handling

| Input | Error Message |
|---|---|
| Letter in a binary number | `Invalid binary digit: x` |
| Digit 8 or 9 in an octal number | `Invalid octal digit: x` |
| Non-hex character in hex input | `Invalid hex digit: x` |
| Non-integer menu input | Prompts again until valid |

---

## Requirements

- Java 8 or higher
- No external libraries needed
