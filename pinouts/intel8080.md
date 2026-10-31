# Interesting Intel 8080 pins

| Intel 8080 Pin | Name        | Type   | Description                                       |
|----------------|-------------|--------|---------------------------------------------------|
| 1              | A10         | Output | Address Bus Bit 10                                |
| 2              | GND         | Power  | Ground Reference (0V)                             |
| 3              | D4          | In/Out | Data Bus Bit 4                                    |
| 4              | D5          | In/Out | Data Bus Bit 5                                    |
| 5              | D6          | In/Out | Data Bus Bit 6                                    |
| 6              | D7          | In/Out | Data Bus Bit 7                                    |
| 7              | D3          | In/Out | Data Bus Bit 3                                    |
| 8              | D2          | In/Out | Data Bus Bit 2                                    |
| 9              | D1          | In/Out | Data Bus Bit 1                                    |
| 10             | D0          | In/Out | Data Bus Bit 0                                    |
| 11             | -5V (VBB)   | Power  | Substrate Bias Power Supply (-5V)                 |
| 12             | RESET       | Input  | Resets Program Counter to 0000H                   |
| 13             | HOLD        | Input  | Requests CPU to yield bus control (for DMA)       |
| 14             | INT         | Input  | Interrupt Request                                 |
| 15             | Phase2      | Input  | Phase 2 Clock Input                               |
| 16             | INTE        | Output | Interrupt Enable Status                           |
| 17             | DBIN        | Output | Data Bus In (signals CPU is ready to read)        |
| 18             | WR          | Output | Write Control (active low, data valid on bus)     |
| 19             | SYNC        | Output | Synchronization signal for start of machine cycle |
| 20             | +5V (VCC)   | Power  | Main Power Supply (+5V)                           |
| 21             | HLDA        | Output | Hold Acknowledge (CPU has released buses)         |
| 22             | Phase1      | Input  | Phase 1 Clock Input                               |
| 23             | READY       | Input  | Memory/IO Ready Signal (causes WAIT state if low) |
| 24             | WAIT        | Output | CPU is in a Wait State                            |
| 25             | A0          | Output | Address Bus Bit 0                                 |
| 26             | A1          | Output | Address Bus Bit 1                                 |
| 27             | A2          | Output | Address Bus Bit 2                                 |
| 28             | +12V (VDD)  | Power  | Main Power Supply (+12V)                          |
| 29             | A3          | Output | Address Bus Bit 3                                 |
| 30             | A4          | Output | Address Bus Bit 4                                 |
| 31             | A5          | Output | Address Bus Bit 5                                 |
| 32             | A6          | Output | Address Bus Bit 6                                 |
| 33             | A7          | Output | Address Bus Bit 7                                 |
| 34             | A8          | Output | Address Bus Bit 8                                 |
| 35             | A9          | Output | Address Bus Bit 9                                 |
| 36             | A15         | Output | Address Bus Bit 15                                |
| 37             | A14         | Output | Address Bus Bit 14                                |
| 38             | A13         | Output | Address Bus Bit 13                                |
| 39             | A12         | Output | Address Bus Bit 12                                |
| 40             | A11         | Output | Address Bus Bit 11                                |

