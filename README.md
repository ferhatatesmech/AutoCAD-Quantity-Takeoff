# AutoCAD Smart Quantity Takeoff Engine (AutoLISP / DCL)

An advanced automation script written in AutoLISP and DCL (Dialog Control Language) designed for AutoCAD users, architects, and quantity surveyors. This tool automates the tedious process of material and area takeoff by dynamically parsing drawing databases and calculating totals organized strictly by layers.

## 🚀 Key Features

* **Dual Mode Takeoff:** Supports both **Linear Takeoff** (Lines, Polylines, Polyline arcs) and **Area Takeoff** (Closed polylines, Hatches, Circles).
* **Smart Unit Detection:** Automatically queries the drawing database (`INSUNITS`) to identify whether the project is modeled in **Meters (m), Centimeters (cm), or Millimeters (mm)**. If unspecified, it triggers an estimation algorithm based on geometric scale.
* **Modern GUI Table Interface:** Displays real-time calculations inside a clean, grid-aligned, native Windows Pop-up Dialog Box (DCL Grid Layout) with zero clutter.
* **No Overhead / Garbage-Free:** Dynamically generates interface files in the system's temporary directory and clears them safely upon closing.
* **Multi-Format Export Options:** Built-in hooks for future or direct deployment to Excel (.CSV) and Text (.TXT) file formats.

---

## 🛠️ Technical Stack & Methods Used

* **Language:** AutoLISP / Visual LISP (VLX)
* **UI Framework:** DCL (Dialog Control Language)
* **Core Math Engines:** Utilizes `vlax-curve-getDistAtParam` for absolute geometric accuracy on lines/arcs, bypassing fragile standard ActiveX property calls.
* **Error Trapping:** Wrapped inside `vl-catch-all-apply` loops to avoid fatal crashes when selecting unclosed or zero-property objects.

---

## 📖 How To Use

1.  Download or clone the `quantity.lsp` file.
2.  Open your project in AutoCAD.
3.  Type `APPLOAD` in the command line, select `quantity.lsp`, and click **Load**.
4.  Type `QUANTITY` in the command line to initiate the engine.
5.  Choose your option (`Area` or `Line`), select your drawing elements, and view your structured report.

---

## 📋 Sample Output Structure

When executed inside the pop-up window, the layout maps data dynamically as follows:

LAYER NAME               TOTAL LENGTH (m)
============================================================
MB_DOMESTIC_WATER        142.55
TRL_HEATING_FLOW         87.90
0_HVAC_DUCTS             312.10

<img width="2289" height="1490" alt="image" src="https://github.com/user-attachments/assets/40b920ff-8502-4c45-ab89-18d901a62529" />

<img width="2312" height="1283" alt="image" src="https://github.com/user-attachments/assets/6351b6af-cfa6-4e36-b65d-f7c2297cda5f" />

<img width="2363" height="1221" alt="image" src="https://github.com/user-attachments/assets/95dd21ae-ed3a-46cc-81f3-e4fc5c0c44d2" />

<img width="2256" height="1258" alt="image" src="https://github.com/user-attachments/assets/28b2a639-31fe-46ab-a89c-33f1309b08b5" />





