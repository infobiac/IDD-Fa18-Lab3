# Data Logger (and using cool sensors!)

*A lab report by **Christophe Rimann**.*

## In The Report

## Part A.  Writing to the Serial Monitor
 
**a. Based on the readings from the serial monitor, what is the range of the analog values being read?**
We can see that values range from 0-1023.
 
**b. How many bits of resolution does the analog to digital converter (ADC) on the Arduino have?**
Given that it has 1024, values, and 2^10 bits, my initial guess would be 10 bits. We can confirm that value [here](https://learn.sparkfun.com/tutorials/analog-to-digital-conversion)!


## Part B. RGB LED

**How might you use this with only the parts in your kit? Show us your solution.**

This question was updated to not include this part.

## Part C. Voltage Varying Sensors 
 
### 1. FSR, Flex Sensor, Photo cell, Softpot

**a. What voltage values do you see from your force sensor?** My force sensor ran from an absolute max of around 1014 (although it was mostly stable at around 1010). The stable min I could reach was 297, with occasional fluctuations to around 290. 

**b. What kind of relationship does the voltage have as a function of the force applied? (e.g., linear?)** The relationship does not appear to be linear; rather it seems to be one of diminishing marginal returns. As I press a lot harder, the dip voltage drops decreasingly less.

**c. Can you change the LED fading code values so that you get the full range of output voltages from the LED when using your FSR?**
I don't believe so. This is because we need to change the voltage of each color independent of each other simultaneously in order to get every possible value. If we had two other voltage varying resistors, perhaps we could, but independently, we cannot. 

**d. What resistance do you need to have in series to get a reasonable range of voltages from each sensor?**

**e. What kind of relationship does the resistance have as a function of stimulus? (e.g., linear?)**

### 2. Accelerometer
 
**a. Include your accelerometer read-out code in your write-up.**

### 3. IR Proximity Sensor

**a. Describe the voltage change over the sensing range of the sensor. A sketch of voltage vs. distance would work also. Does it match up with what you expect from the datasheet?**

**b. Upload your merged code to your lab report repository and link to it here.**

## Optional. Graphic Display

**Take a picture of your screen working insert it here!**

## Part D. Logging values to the EEPROM and reading them back
 
### 1. Reading and writing values to the Arduino EEPROM

**a. Does it matter what actions are assigned to which state? Why?**

**b. Why is the code here all in the setup() functions and not in the loop() functions?**

**c. How many byte-sized data samples can you store on the Atmega328?**

**d. How would you get analog data from the Arduino analog pins to be byte-sized? How about analog data from the I2C devices?**

**e. Alternately, how would we store the data if it were bigger than a byte? (hint: take a look at the [EEPROMPut](https://www.arduino.cc/en/Reference/EEPROMPut) example)**

**Upload your modified code that takes in analog values from your sensors and prints them back out to the Arduino Serial Monitor.**

### 2. Design your logger
 
**a. Insert here a copy of your final state diagram.**

### 3. Create your data logger!
 
**a. Record and upload a short demo video of your logger in action.**
