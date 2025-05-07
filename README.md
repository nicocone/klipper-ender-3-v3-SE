# klipper-ender-3-v3-SE
printer.cfg printer area addressed


Hi everyone!

I'm new to GitHub, but since the files from @shubham0x13 [https://github.com/shubham0x13/ender-3-v3-se-klipper] helped me a lot, I just wanted to contribute my two cents.

In this printer.cfg file, I’ve corrected the endstop values for the X and Y axes to properly center the print area.

Explanation:

I noticed that the bed of the Ender 3 V3 SE is actually 235mm x 235mm. The previous values caused my printer to treat (0,0) as the physical corner of the bed, which is incorrect. (This results in prints being off-center.)

So what I did was update the endstop values to make (0,0) align with the intended origin.

I hope this small contribution helps someone in the future!

#IMPORTANT:

I believe that maybe other Ender 3 v3 SE printers can have more or less steps from the endstops to the 0,0 position. So I recommend to always check these values and make you required changes.

For X axe:

[stepper_x]

position_endstop: -12 <-------------------You need to change this value

position_min: -12 <-------------------This one should match the value avobe



For Y axe:

[stepper_y]

position_endstop: -24 <-------------------You need to change this value

position_min: -24 <-------------------This one should match the value avobe

