# LED

This repository is part of a larger effort project to create a custom control
application to control APA102 LED strip lights hooked up to a Raspberry Pi computer.

The **led_pi** repo is the pi-side code that should eventually be able to process
incoming requests on a custom port. To start, though, the program will run only on
the Pi with a GUI to control the lights. 

This project is being developed using Python 3.7.3.

## Info & Resources

The LED light strip used for this project has 60 individually addressable LEDs.
This means that we can individually access and change each individual LED light on the strip.

The LED light strip uses the APA102 standard. To the programmer, this means we will use
an APA102 library in Python. The library we will use to communicate with the light strip
is [here](https://github.com/tinue/apa102-pi). Please pay particular attention to the
[APA102 class](https://github.com/tinue/apa102-pi/blob/main/apa102_pi/driver/apa102.py) 
defined in Python.

## Tasks

Updated December 28, 2020.

- [ ] Build a simulator so that the lights can be developed remotely
    1. [ ] Create a GUI that shows the full light strip with all lights turned off
    2. [ ] Create a function to turn all the lights on
        1. [ ] Add a button to the GUI to turn all the lights on/off
    3. [ ] Add functionality to change the color of (all) the lights
        1. [ ] Add the ability to change one LED at a time
	2. [ ] Add the abilility to change one or more possibly non-consecutive LED lights at a time
	    - Basically, this means the user should be able to take advantage of the individually addressable LEDs, and set any 1 or more of them to a certain color at a time.
- [ ] Open a port so the program can recieve requests remotely.
    1. [ ] Connect pi via ethernet
    2. [ ] Set up port forwarding on the router
    3. [ ] Test that pi can receive data from inside home network
    4. [ ] Test that pi can receive data from outside home network