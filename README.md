## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/earthedstem/IOT_Smart_City** and import

## Edit this project ![Build status badge](https://github.com/EarthEdSTEM/IOT_Smart_City/blob/7b74ac94eb6d0325710eb0919fe348b879f3c6e0/workflows/MakeCode/badge.svg)

To edit this repository in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/earthedstem/IOT_Smart_City** and click import

## Supported targets

* for PXT/microbit
(The metadata above is needed for package search.)

```package
environment=github:sunnyrainwss/pxt-iot-environment-kit
iot=github:sunnyrainwss/pxt-iot-environment-kit
```

## Blocks preview

This image shows the blocks code from the last commit in master.
This image may take a few minutes to refresh.

![A rendered view of the blocks](https://github.com/earthedstem/IOT_Smart_City/raw/master/.github/makecode/blocks.png)

#### Metadata (used for search, rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>

#Tutorial
### @explicitHints false
### @activities 1
```template
basic.forever(function () {})
```
# EarthEd IOT Smart City Tutorial
## Introduction
### Introduction step @showdialog
![](https://github.com/EarthEdSTEM/IOT_Smart_City/raw/main/Images/SmartCityBanner.jpg)

Welcome to the EarthEd IoT Smart City Tutorial. In this tutorial, you will learn how to use certain input and output devices with your micro:bit computer and IoTbit shield.<br>
This tutorial contains sections describing how to:
1. Connect the micro:bit computer
2. Code the LED module
3. Code the Contact Sensor
4. Code the Water Level Sensor


<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 1 - Connect & Test the micro:bit
<!---  Designed to test if the microbit is working --->
### Step 1 Connecting the microbit 
Plug in your micro:bit to connect!
----------------------------------
Connect the micro:bit to your your computer using the USB cable.
Need to know how to connect your micro:bit to your computer? [Watch this video](https://www.youtube.com/watch?v=qSjMDG84bMY)<br>
Skip to Activity 2 if you have done it previously.

### Step 2 @fullscreen
Create some simple code to test your micro:bit. You won't need the SensorBit for this.
------------------------------------
In the Basic Tab, place the ``||basic:show leds||`` block in the ``||basic:forever||`` block and draw a pattern.
```blocks
basic.forever(function () {
    basic.showLeds(`
        # . # . #
        . # # # .
        # # # # #
        . # # # .
        # . # . #
        `)
})
```
### Step 3 - Upload the code
Pair and Upload your code
-------------------------
Clicking ``|Download|`` opens a dialogue box. From here, you can download the file to your computer and then transfer it (upload) using File Explorer, or click ``|Pair|``. If it is already attached by USB, ``|Pair|`` sends your code directly to the memory in the micro:bit.

[Need more help connecting? Click here.](https://www.youtube.com/watch?v=qSjMDG84bMY)


<!---------------------------------------------------------------  
-------------------------  NEW ACTIVITY -------------------------
----------------------------------------------------------------->
## Activity 2 - Control a LED

### Step 1 - Collect the parts. @unplugged
Control a LED
=============
In this activity you will use a [variable](https://launchschool.com/books/ruby/read/variables) to control when a LED (light Emitting Diode) is turned on or off.<br> 
Parts Needed: 1x IoT Smart City LED, 1x IoT:Bit sheild, 1x micro:bit, 1x Connector Wire<br>
![Parts Needed: 1x IoT Smart City LED, 1x IoT:Bit sheild, 1x micro:bit, 1x Connector Wire](https://raw.githubusercontent.com/EarthEdSTEM/IOT_Smart_City/main/Images/IoT_LED_Parts_List.svg)


### Step 2 - Connect Up!
Physical Connections
____________________
1. Plug the micro:bit into the SensorBit sheild.
2. Use the wire to connect the LED to Pin 2 on the SensorBit sheild.
3. Connect the other end of the wire to the LED.
![image](https://raw.githubusercontent.com/EarthEdSTEM/IOT_Smart_City/main/Images/IoT_LED_Connections.svg)

### Step 3 - Prepare to Code!
1. Clear the previous blocks by dragging them to the menu bar.
2. Place a ``||basic:forever||`` block and a ``||on start||`` onto the work space.
![Deleting code](https://raw.githubusercontent.com/EarthEdSTEM/IOT_Smart_City/main/Images/Delete_code.png)

### Step 4 - Create Variables (Setting the Environment)
Coding: Creating Variables
---------------------------------
Variables are containers that hold a value. For this task, we will use the values 1 for 'true' and 0 for 'False'.
We will start by creating a new variable, adding it and then setting it to 'false'.
1. Click ``||Variables: Make a Variable...||`` to create a variable and call it ButtonAPress.
2. Go to ``||Variables||`` and place the ``||Variables:Set ButtonAPress to||`` block inside the ``||Basic:on Start||`` block.
3. Check that the value of the ``||Variables:Set ButtonAPress to||`` block is set to 0 (for false).
![Making a variable](https://raw.githubusercontent.com/EarthEdSTEM/IOT_Smart_City/main/Images/Make_variable.jpg)
Each time the program starts the value of ButtonAPress will be '0'.

### Step 5 - Add a Conditional Block
Coding: Add an If block
---------------------------------
The switch for turning on the LED will be the A button on the micro:bit. We will use the 'If...then' Logic Block to check if the A button is pressed and if the LED is off. If both are true the LED is set to on.
1. Place a ``||logic:if||`` block from the Logic menu into the ``||basic.forever||`` block.

```blocks
let ButtonAPressed = 0
basic.forever(function () {
    if () {
     
})
```

### Step 6 - Add a Conditional Block
Coding: Set conditions
---------------------------------
1. Place a Boolean ``||logic:and||`` block from the Logic Menu into the placeholder at the top of the ``||logic:if||`` block. <br>
**Note that the placeholder has pointed ends. Only blocks with pointed ends can fit in the placeholder. The ``||logic:and||`` block has two placeholders with rounded ends for adding variables and values.
2. Place a Comparison ``||logic:equals||`` block from the Logic Menu into the placeholder at the top of the ``||logic:if||`` block. Add a ``||variables:ButtonAPress||`` and a value of 0.


```blocks
let ButtonAPressed = 0
basic.forever(function () {
    if (input.buttonIsPressed(Button.A) && ButtonAPress == 0) {
    
})
```

### Step 7 - Add a Conditional Block
Coding: If True
---------------------------------
The 'if' block checks if a condition is 'true' and executes commands if it is. Here, we enable Pin 2 then pause, allowing the user to remove their finger from Button A.
1. Add a ``||pins:digital write pin||`` block to the ``||logic:if||`` and set it to 'P2' and 1.
2. Add a ``||control:waitMicros||`` and set it to 240 milliseconds. this will allow time for the button to be released.
3. Set the ButtonAPressed variable to 1 (True).

```blocks
let ButtonAPressed = 0
basic.forever(function () {
    if (input.buttonIsPressed(Button.A) && ButtonAPress == 0) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        control.waitMicros(242)
        ButtonAPressed = 1
    
})
```
### Step 8 - Program Continued
Coding: Turning the LED off
---------------------------------
Now we add what will happen if the condition is not true. 
1. Click the 'plus' symbol on the if block to add an 'else' condition.
2. Add blocks to turn off the LED. Try it yourself or check the Hint to find out how.

```blocks
let ButtonAPressed = 0
basic.forever(function () {
    if (input.buttonIsPressed(Button.A) && ButtonAPressed == 0) {
        pins.digitalWritePin(DigitalPin.P2, 1)
        control.waitMicros(242)
        ButtonAPressed = 1
    } else {
        if (input.buttonIsPressed(Button.A) && ButtonAPressed == 1) {
            pins.digitalWritePin(DigitalPin.P2, 0)
            control.waitMicros(242)
            ButtonAPressed = 0
        }
    }
})
```



> Open this page at [https://earthedstem.github.io/earthed_servo_tutorial/](https://earthedstem.github.io/earthed_servo_tutorial/)

## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/earthedstem/earthed_servo_tutorial** and import

## Edit this project ![Build status badge](https://github.com/earthedstem/earthed_servo_tutorial/workflows/MakeCode/badge.svg)

To edit this repository in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/earthedstem/earthed_servo_tutorial** and click import

## Blocks preview

This image shows the blocks code from the last commit in master.
This image may take a few minutes to refresh.

![A rendered view of the blocks](https://github.com/earthedstem/earthed_servo_tutorial/raw/master/.github/makecode/blocks.png)

#### Metadata (used for search, rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
