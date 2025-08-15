<h1 align="center">📡 UART Verification using SystemVerilog</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Language-SystemVerilog-blue?style=for-the-badge&logo=verilog" />
  <img src="https://img.shields.io/badge/Methodology-TLM%20&%20CRV-green?style=for-the-badge&logo=checkmarx" />
  <img src="https://img.shields.io/badge/Domain-VLSI%20Verification-orange?style=for-the-badge&logo=semanticscholar" />
</p>

---

## 📖 Project Overview
This project focuses on **functional verification** of a **UART (Universal Asynchronous Receiver/Transmitter)** using **SystemVerilog** with **Transaction-Level Modeling (TLM)** and **Constrained-Random Verification (CRV)**.  
The testbench architecture is modular and reusable, with a **custom generator, driver, monitor, scoreboard, and environment** to ensure protocol correctness, timing compliance, and data integrity.

---

## 🛠️ Key Components Implemented

- **📄 Transaction Class** – Defines UART frame fields (start bit, data bits, parity, stop bit) with randomization constraints for CRV.
- **🚗 Driver** – Sends UART transactions to the DUT at the specified baud rate.
- **🕵️‍♂️ Monitor** – Observes TX/RX activity and sends captured frames to the scoreboard.
- **📊 Scoreboard** – Compares DUT output against expected data for integrity checks.
- **🎲 Constrained-Random Stimulus** – Generates a variety of valid and error scenarios (framing error, parity error, baud mismatch).
- **🔁 UART DUT** – Implements transmitter and receiver modules with configurable parameters.

---


---

## 📈 Verification Flow
1. **Transaction Generation** – Constrained-random UART frames are created.
2. **Driver** – Sends frames to DUT TX/RX through interface.
3. **DUT Execution** – UART transmitter/receiver processes serial data.
4. **Monitor** – Captures serial output and converts back to parallel data.
5. **Scoreboard** – Compares DUT output with expected data to detect mismatches.
6. **Coverage** – Ensures all protocol conditions, error types, and baud rate scenarios are tested.

---

## ✅ Achievements in This Project
- Designed a **reusable and modular UART verification environment**.
- Implemented **Transaction-Level Modeling (TLM)** for better maintainability.
- Used **Constrained-Random Verification** to cover all corner cases.
- Verified UART **protocol correctness**, **baud rate timing**, and **error handling**.
- Implemented **self-checking testbench** for automated pass/fail detection.
- Achieved high coverage across **normal**, **framing error**, **parity error**, and **baud mismatch** cases.

