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
<img width="451" alt="image" src="https://github.com/user-attachments/assets/b95ff00d-9820-4b77-86ed-8940c09d229f" />

  

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

