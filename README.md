# IDD-Fa18-Lab1: Blink!

**A lab report by Lois Lee**

## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**
Brown, Black, Brown, Gold
 
**b. What do you have to do to light your LED?**
Hook the pushbutton up to power, put the positive end of the LED to the other end of the pushbutton, attach the 100 ohm resistor from the remaining end of the LED to ground. Push the button to connect the LED to the power source.


## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**
In the setup, the output LED is currently the builtin LED which can be seen in : `pinMode(LED_BUILTIN, OUTPUT);` what we want to do is change that to a pin that we've connected the LED to. For example, if pin 13, `pinMode(13, OUTPUT);`

**b. What line(s) of code do you need to change the rate of blinking?**

The following code is what is in the loop. The `delay(1000)` show that the arduino is blinking every 1 second. We can simply change the 1000 value to change the rate of blinking. 
```
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```

**c. What circuit element would you want to add to protect the board and external LED?**
A resistor, just to prevent potential short circuiting.
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**
0.013 is how long researchers at MIT say it takes for the human brain to process entire images, so when the delay is 10, or .010 seconds, it makes it hard for us to detect the rapid change.



**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**
Yes, it turns all the way up to max brightness and appears to turn completely off.


## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

Change the led variable to `int led = 11;`     

**b. What is analogWrite()? How is that different than digitalWrite()?**
analogWrite() allows us to write a range of voltages rather than just 0 and 5V.


## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
