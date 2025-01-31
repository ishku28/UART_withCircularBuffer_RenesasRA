# UART Project for E2 Studio

This project demonstrates the use of UART with interrupts on Renesas microcontrollers using E2 Studio. It includes a circular buffer implementation for handling incoming UART data.

## Getting Started

These instructions will guide you through setting up and running the project in E2 Studio.

### Prerequisites

- **E2 Studio**: Ensure you have E2 Studio installed. You can download it from the [Renesas website](https://www.renesas.com/).
- **FSP (Flexible Software Package)**: Make sure you have the latest version of the FSP installed.

### Generating the Project

1. **Open E2 Studio**: Launch E2 Studio on your computer.
2. **Create a New Project**:
   - Go to `File` > `New` > `Renesas C/C++ Project`.
   - Select the appropriate board and device.
   - Choose `FSP` as the project type.
   - Name your project and click `Finish`.

3. **Configure FSP**:
   - Open the **FSP Configuration** perspective.
   - Configure the UART module:
     - Set the baud rate to 115200.
     - Enable interrupts for RX and TX.

### Importing the Project Files

1. **Copy Source Files**:
   - Copy the provided `uart.c` and header files into the `src` directory of your project.
   - Ensure all necessary header files are included in the `include` directory.

2. **Update the Build Configuration**:
   - Right-click on the project in the Project Explorer.
   - Select `Properties`.
   - Under `C/C++ Build`, ensure the include paths are set correctly to find all header files.

### Building the Project

1. **Build the Project**:
   - Click on the `Build` button or go to `Project` > `Build Project`.
   - Ensure there are no build errors. Resolve any issues if they arise.

### Running the Project

1. **Connect Your Board**:
   - Connect your Renesas board to your computer via USB.
   - Ensure the correct COM port is selected for UART communication.

2. **Download and Debug**:
   - Click on the `Debug` button to download the program to the board.
   - Use the E2 Studio debugger to step through the code if necessary.

3. **View UART Output**:
   - Use a terminal application (e.g., Tera Term, PuTTY) to connect to the UART COM port.
   - Set the baud rate to 115200.

### Notes

- The circular buffer size is defined as 4. Adjust `CIRCULAR_BUFFER_SIZE` in `uart.c` if needed.
- Handle buffer overflows gracefully as implemented in the `user_uart_callback` function.

### License

This project is licensed under the BSD-3-Clause License. See the `LICENSE` file for details.

### Acknowledgments

- Renesas Electronics Corporation for providing the hardware and software tools.

For further assistance, please refer to the Renesas documentation or contact the support team.
