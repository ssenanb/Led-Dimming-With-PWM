# Led-Dimming-With-PWM

->Project Overview
This project demonstrates how to control the brightness of an LED using Pulse Width Modulation (PWM) on an STM32F0 microcontroller. A user button (connected to pin PA0) is used to adjust the LED brightness, increasing it in increments, and resetting it to 0 when a certain threshold is reached. The project uses interrupts to detect button presses, enabling efficient and responsive input handling.

->Features
PWM Control: Controls the LED brightness by adjusting the duty cycle.
Button Interrupt: The button press triggers an interrupt to increment the duty cycle.
Brightness Loop: The LED's brightness increases by 2% each time the button is pressed, and resets to 0% once the duty cycle reaches 100%

->Hardware Requirements
STM32F0 Discovery board or similar STM32 microcontroller.
An LED and a current-limiting resistor.
A push button connected to PA0.
Jumper wires for connections.

->Software Requirements
* STM32CubeMX (for configuration and code generation).
* STM32 HAL library.
* STM32CubeIDE.

->Pin Configuration
PA0: Button input with external interrupt (rising edge).
PWM Output (PA8): Connected to an appropriate pin, configured for PWM.

->Circuit Diagram


->Project Setup
1-Configure the MCU: Use STM32CubeMX to configure the necessary peripherals:
* GPIO pin PA0 as input with external interrupt.
* PWM output on an appropriate pin (PA8).
* Timer for PWM signal generation.

2-Generate Code: Once the configuration is complete, generate the code and open it in STM32CubeIDE.

3-Write the Application:
* Implement the interrupt callback function to handle button presses.
* Use HAL_TIM_PWM_Start() to start PWM output.
* Adjust the duty cycle in the interrupt callback.

->Code Explanation
PWM Setup: A timer is used to generate the PWM signal, with the duty cycle adjusted based on the button press.
Button Interrupt: The button triggers an external interrupt on PA0, which increments the duty cycle of the PWM. Once the duty cycle reaches 100%, it resets to 0.

CIRCUIT INSTALLATION -> https://github.com/ssenanb/Led-Dimming-With-PWM/blob/main/WhatsApp%20G%C3%B6rsel%202025-04-27%20saat%2001.26.09_9246eb49.jpg?raw=true
