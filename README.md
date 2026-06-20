# RISC-V-Single-Cycle-Processor
32-bit Single Cycle RISC-V Processor designed in Verilog with verification testbenches.
# 32-Bit Single-Cycle RISC-V Processor

A complete RTL implementation of a 32-bit Single-Cycle RISC-V Processor using Verilog HDL. This project demonstrates the fundamental architecture of a RISC-V processor, including instruction fetch, decode, execute, memory access, and write-back operations.

---

 📋 Project Overview

This project implements a basic 32-bit RISC-V processor based on a Single-Cycle Architecture. The processor executes each instruction in a single clock cycle and supports arithmetic, memory, and branch operations.

The primary objective of this project was to gain hands-on experience in:

* RISC-V Architecture
* RTL Design using Verilog HDL
* Processor Datapath Design
* Control Signal Generation
* Functional Verification using Testbenches
* Waveform Analysis using GTKWave

---

✨ Features

* 32-bit RISC-V Architecture
* Single-Cycle Processor Design
* Modular RTL Implementation
* Instruction Fetch and Decode
* Arithmetic and Logic Operations
* Load and Store Memory Operations
* Branch Instruction Support
* Immediate Value Generation
* Functional Verification with Testbenches

---

 📁 Repository Structure

```text
RISC-V-Single-Cycle-Processor/
│
├── README.md
│
├── rtl/
│   ├── alu.v
│   ├── control.v
│   ├── imm_gen.v
│   ├── reg_file.v
│   ├── data_mem.v
│   ├── instr_mem.v
│   ├── pc.v
│   └── top.v
|   |__top_tb.v

---

 🏗️ Processor Architecture

The processor consists of the following modules:

 Program Counter (PC)

* Stores the address of the current instruction.
* Updates the Program Counter for the next instruction fetch.

 Instruction Memory

* Stores machine instructions.
* Supplies instructions based on the current PC value.

 Control Unit

* Decodes instruction opcodes.
* Generates control signals for processor operation.

 Register File

* Contains 32 general-purpose registers.
* Supports two read ports and one write port.

 Immediate Generator

* Extracts immediate values from instructions.
* Supports I-Type, S-Type, and B-Type formats.

 Arithmetic Logic Unit (ALU)

* Performs arithmetic operations.
* Generates a Zero flag for branch decisions.

 Data Memory

* Supports Load Word (LW) and Store Word (SW) operations.
* Stores and retrieves data.

 Top Module

* Integrates all processor components.
* Implements the complete datapath.



 📚 Supported Instructions

| Instruction | Type   | Description       |
| ----------- | ------ | ----------------- |
| ADD         | R-Type | Register Addition |
| ADDI        | I-Type | Add Immediate     |
| LW          | I-Type | Load Word         |
| SW          | S-Type | Store Word        |
| BEQ         | B-Type | Branch if Equal   |

 ⚙️ Working Principle

The processor executes instructions through the following stages:

 1. Instruction Fetch

* PC provides the instruction address.
* Instruction Memory fetches the instruction.

2. Instruction Decode

* Control Unit decodes the opcode.
* Register File reads source operands.

 3. Immediate Generation

* Immediate Generator extracts and sign-extends immediate values.

 4. Execute

* ALU performs arithmetic or comparison operations.

 5. Memory Access

* Data Memory performs read/write operations for load and store instructions.

 6. Write Back

* Results are written back into the Register File.

 7. PC Update

* PC increments by 4 for normal execution.
* For branch instructions, PC jumps to the target address when the branch condition is satisfied.

---

🧪 Verification

Each module was verified independently using dedicated Verilog testbenches.

 Verified Modules

* ALU
* Control Unit
* Immediate Generator
* Data Memory
* Register File
* Program Counter
* Top-Level Integration

 Verification Method

* Functional Simulation
* Self-Checking Testbenches
* Module-Level Verification
* Top-Level Integration Testing

---

 🛠️ Tools Used
* EDA Playground
* Xilinx Vivado


 📈 Learning Outcomes

Through this project, I gained practical experience in:

* RISC-V Processor Architecture
* RTL Design and Coding
* Datapath and Control Path Design
* Memory Interface Design
* Processor Verification
* Testbench Development
* Waveform Debugging



 🚀 Future Improvements

* Add logical operations (AND, OR, XOR)
* Add comparison instructions (SLT)
* Support additional RISC-V instructions
* Implement a 5-Stage Pipelined Architecture
* Add Hazard Detection Unit
* Add Forwarding Unit
* Improve processor performance.

 👩‍💻 Author

 S. Kanimozhi

 Electronics and Communication Engineering (ECE)

 Chennai Institute of Technology


