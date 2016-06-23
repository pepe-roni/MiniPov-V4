# MiniPov-V4
The MiniPov uses x3 AAA batteries in series as a 4.5V source. The source flows into a 100 uF capacitor which provides a stable voltage, compensating for voltage drops with the stored charge within the parallel plates held by an electric field. This stabilized voltage flows into a 2.2k ohm resistor and a 47 ohm resistor and then into the arduino based IC. The IC, a microcontroller, controls the LEDs timings and takes the timing from a potentiometer (10k ohm) which determines the speed at which the LEDs displays text. The IC uses a ceramic resonator (12Mhz) as a clock for LED timings. Information from the IC to determine color and timings are then moved to the NPN transistors after reducing voltage with a 2.2k ohm resistor. The NPNnpn transistor regulates voltage of the red, green and blue channels. Each LED has 4 pins due to red, green, and blue inputs and then a ground. The LEDs receive a lower voltage after passing through a 47 ohm resistor. The IC can be programmed to display different text/images through a Processing generated sketch where you can import the files. The USB B input on the board is filtered by two diodes (3.7v) to ensure there is no backflow of current in an event of ESD.  

I could not get the firmware of the MiniPov to work on Windows 10, as drivers were designed for Windows 8. I used an instructor’s PC which had Windows 7 to download drivers and load the firmware. Before that however I retried installing the drivers many times and just to check I re-soldered the USB B port and tried my peer’s Windows 10 computer and it did not work. 

I discovered a new component which I previously did not know of which is the ceramic resonator. I learned that it is a piezoelectric ceramic with pins and when powered it generates an alternating/oscillating signal of a specific frequency, in this case 12Mhz. The thickness of the ceramic determines the output resonant frequency. I also found out that diodes are used on data lines to protect against ESD (electrostatic discharge), whether from a failed component or from human error, e.g. contact with PCB.

To be completely honest this MiniPov thing really rather just looks cool and has really little functionality. The MiniPov was designed as a text or image display that you wave around in front of someone. Then the flashing of LED’s is a set timing would allow you to see the text you uploaded onto it (by taking advantage of our eyes’ refresh rates). However, it is extremely hard to actually see text so I’ll just take this starter project as a source of components (I will mercilessly take it apart) and of course a learning experience.
