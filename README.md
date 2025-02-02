# SHA-256 Implementation in Verilog

## Overview
This project implements the **SHA-256 cryptographic hash function** in Verilog. The design follows the standard **FIPS 180-4** specification and is optimized for a sequential approach. It processes 512-bit message blocks with 64 compression rounds per block.

## Features
- Fully functional **SHA-256 hashing algorithm** in Verilog
- Supports **512-bit message blocks** with sequential processing
- Optimized for **hardware-based cryptographic applications**
- Can be integrated into custom **RISC-V processors** for security applications
- Outputs a **256-bit digest** in hexadecimal format

## System Components
- **SHA-256 Core**: Performs the hashing operation
- **Message Scheduler**: Expands 16 words into 64 words for processing
- **Compression Function**: 64 rounds using bitwise logical operations and modular addition
- **Output Formatter**: Converts the final 256-bit hash to hexadecimal

## Implementation Details
- The design uses **a sequential approach**, meaning one round per clock cycle.
- Requires **64 clock cycles per 512-bit block** (excluding preprocessing and finalization).
- The implementation follows **pipelined architecture** to optimize performance.
- Can be interfaced with an **LCD or 7-segment display** for real-time hash output.

## Design
 - The input was taken from ps-ii keyboard and the output was displayed on an lcd.
 - The core took 70 cycles to complete while displaying it on lcd(which needed delay) took many clock cycles.
 - The circuit followed a sequential approach by calculating round value iteration wise.

## RTL
 <img width="754" alt="image" src="https://github.com/user-attachments/assets/72c044ac-c18f-4498-8a2b-e7ac8fb0d044" />

## Top level state machine
 <img width="730" alt="image" src="https://github.com/user-attachments/assets/79e2e188-f45e-4d89-9d92-f2881ab0ee5a" />



  

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/singhpalash/sha256_verilog.git
   ```
2. Open the project in your preferred Verilog simulation tool (ModelSim, Verilator, etc.).
3. Run the simulation and provide a test input message.
4. Observe the **256-bit hashed output** in the simulation waveforms or hardware display.

## Future Improvements
- **Parallelized architecture** to reduce hashing time.
- **Integration with RISC-V custom instructions** for cryptographic operations.

## Author
Palash Singh   

## References
- [SHA-256 Specification (FIPS PUB 180-4)](https://csrc.nist.gov/publications/detail/fips/180/4/final)
- [Verilog HDL Documentation](https://ieeexplore.ieee.org/document/8978423)

