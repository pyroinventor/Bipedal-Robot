# Bipedal-Robot
A simple 4-servo bipedal robot on the ESP32 platform

# Overview
I wanted to build a bluetooth controlled robot, but didn't want to do a wheeled vehicle. After some research, I came across this simple bipedal design know as "Bob the Biped" from [this](https://www.instructables.com/BoB-the-BiPed/) instructable. It only required 4 servos to execute a pretty smooth walking gait, so I decided to give it a shot.

# Materials
* 4 x 9g servos
* ESP-32
* 3D printed [parts](https://www.thingiverse.com/thing:43708)
* 4 x control horns
* 12 x servo screws
----
# Assembly
Assembly is pretty straightforward. The key is to center the servos before attatching the control horns. This can be done my running any servo example in the arduino IDE and setting the angle to 90.
----
# Code
I didn't end up using the instructable code, but instead went with a trig approach. The code generates a table of values using the sine and cosine functions, then reads out, scales, and writes the values to the servos. This creates a smooth walking gait that is really satisfying to watch. The speed, amplitude, turning scalers, and step resolution can all be configured in the code. Here's the latest revision of what I used.  

