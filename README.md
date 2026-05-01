## STM32 UART Interrupt — Terminal LED Control

**Board:** STM32 Nucleo F413ZH  
**IDE:** STM32CubeIDE  
**Library:** HAL  
**Baud Rate:** 115200  

### What it does
Controls 3 on-board LEDs via UART terminal commands.
Sends "Ready" message on startup, then listens for commands.

### Command Format
| Command | Action     |
|---------|------------|
| LED1\n  | Toggle LD1 |
| LED2\n  | Toggle LD2 |
| LED3\n  | Toggle LD3 |

### Key concepts
- UART receive interrupt via RXNE flag
- Direct data register (DR) access
- Newline-terminated command parsing
- Buffer overflow protection
- Volatile shared variables across source files
- Extern variable declarations between main.c and stm32f4xx_it.c
