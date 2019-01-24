Please include your answers to the questions below with your submission, entering into the space below each question
See [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) for github markdown formatting if desired.

**1. How much current does a single LED draw when the output drive is set to "Strong" with the original code?**

Measured 4.97 mA with the LED on 4.48 mA with the LED off, so a single LED draws 0.49 mA

**2. After commenting out the standard output drive and uncommenting "Weak" drive, how much current does a single LED draw?**

Measured 4.98 mA with the LED on 4.48 mA with the LED off, so a single LED draws 0.50 mA

**3. Is there a meaningful difference in current between the answers for question 1 and 2? Please explain your answer, 
referencing the [Mainboard Schematic](https://www.silabs.com/documents/public/schematic-files/WSTK-Main-BRD4001A-A01-schematic.pdf) and [AEM Accuracy](https://www.silabs.com/documents/login/user-guides/ug279-brd4104a-user-guide.pdf) section of the user's guide where appropriate.**

No.  The Mainboard schematic user LEDs LED100 and LED101 are connected to GPIO pins through a 3K resistor, and this resistor plus the forward voltage drop of the LED
would limit the current through the LED below the weak LED drive strength limit of 1mA given a 3.3V power supply.
Also since the AEM is only able to accurately measure current differences to 0.1 mA above 250uA, a difference of 0.01mA between readings is not significant. 

**4. Using the Energy Profiler with "weak" drive LEDs, what is the average current and energy measured with only LED1 turning on in the main loop?**

4.81mA

**5. Using the Energy Profiler with "weak" drive LEDs, what is the average current and energy measured with both LED1 and LED0 turning on in the main loop?**

4.98mA