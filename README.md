# IDD-Fa19-Lab1: Blink!

**A lab report by Rony Krell

## Part A. Set Up a Breadboard

![Breadboard picture](https://github.com/ronykrell/IDD-Fa18-Lab1/blob/master/breadboard.JPG "Breadboard")

## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

 Red / Light Brown - Red / Light Brown - Black - Black - Dark Brown

**b. What do you have to do to light your LED?**

![Push Button picture](https://github.com/ronykrell/IDD-Fa18-Lab1/blob/master/push_button.JPG "Push Button")

Connect the 5V line to one end of the push button. Connect the other end to the LED and the 270 Ohm resistor. Finally, connect the other end of the resistor to the ground line.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

Had to change LED_BUILTIN to 9 
`
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(9, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(9, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(9, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
`

**b. What line(s) of code do you need to change to change the rate of blinking?**

Had to modify the delay commands in the loop.


**c. What circuit element would you want to add to protect the board and external LED?**
Ground
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

Around 20 ms. We could add a beep along with each blink. The beep would prove that the blinking is working.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.**
[Code for custom blinking program](https://github.com/ronykrell/IDD-Fa18-Lab1/blob/master/custom_blink.ino)

### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[Video Link] (https://www.youtube.com/watch?v=qTb3eDwNrps&feature=youtu.be)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

Yes, the potentiometer acts as a voltage divider - increasing the resistance and decreasing the LED voltage 


## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

Change the LED variable to 11 so that signal goes to pin 11.

**b. What is analogWrite()? How is that different than digitalWrite()?**

 The analogWrite() uses PWM to create a fading effect on the LED on certain outputs. digitalWrite doesn't use PWM.

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
