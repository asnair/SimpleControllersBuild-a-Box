# How to recreate the Smash Box!  (Guide v2.1)
### Guide made by: Simple Controllers
Free to use modify and share.  If you paid for this guide through a third party you have been scammed.  I’m not responsible for misuse or malfunction of any part of this guide.  Use at your own risk.

# Parts
- What you need
- Preparation
- How to do it
- Side notes
- Purchased Stuff
- Credits
- Self Plug 
- Checklist ( )


** (If my in depth tutorial is hard to understand and you don’t want to go into great detail on how a lot of stuff works, just mainly follow the checklist!  It’s a lot simpler easier to follow along!!) **

Link to Youtube Video: https://www.youtube.com/watch?v=5h7IPojhzTc
Link to Reddit Thread: https://www.reddit.com/r/SSBM/comments/5mebc5/how_to_make_your_own_smash_box/

scroll down :D

# Part 1 - What you need:
You are going to need:
- Arduino Mega 2560(1st or 3rd party does not matter) (Also the pro “mini” version works a lot better since you can solder connections) 
- 21 Sanwa Buttons 24mm OSBF/OSBC or the screw in type 
- Logic Controller 5v - 3.3v Bidirectional
- 1k resistor to pull up the line
- Gamecube Extension Cable or spare controller wire (The “Male” end only)
- I recommend using an Official controller.  The extension cables do not have any cable shielding and are just really cheap and not worth using.  Sometimes they even mix up the wire colors so be careful.
- 16”x8”x2” case or something similar (notes on constructing this in side notes below)
- Hit Box released their Kickstarter recently and it was found out that the box is actually 16”x8”x2” instead of 16”x7”x2”.  Sorry!
- 15/16” Spade Bit to cut holes for buttons
- Wires with quick disconnects .110”
- Jumper wires (If you are running the non pro version of Arduino Mega)
- Heatshrink + Solder + Soldering Iron
- On Off switch if you want to toggle DPad
- I also used a portion of the top shell of a broken gamecube controller to alleviate some stress on the cable.  This could be done with other things very easily.
- You also need to download the Nicohood Arduino Library along with my sketch!
## Links:
Nicohood Library:
https://github.com/NicoHood/Nintendo
       
Version 2.0 of my code:
https://github.com/SimpleControllers/SimpleControllersBuild-a-Box
Added a bunch of stuff: 
Axe Style Shield Drops (without modifiers)
Switch/Button on Pin 12 to swap X1, X2, Y1, Y2 to DPAD
Fixed the accidental swapping of X1 with X2, and Y1 with Y2
Angles are fixed to proper smashbox ones
Some random small stuff

(Links to stuff I purchased down below in the sidenotes)





# Part 2 - Prep:
Have the case 16”x8”x2” controller box drilled out with the 21 Sanwa buttons in their desired spots (Attach on off/selector switch for more modes and or dpad)
Link to layout that you can add/remove buttons to (goo.gl/rT3BNP)
Strip the Gamecube Controller cord along with the 6 wires inside. (Note: The cheap Gamecube extension cord you get Online don’t have any cable shielding which may or may not have crosstalk problems also the colors may be mixed up)
http://www.int03.co.uk/crema/hardware/gamecube/gc-control.htm
This guide notes the color coordination of the wires use white, black and green share a common ground
I found that desoldering the wire from a controller and separating the crimped connectors way easier to use than actually stripping each wire.  Especially since the wires are very brittle.
Splice and Solder the Quick Disconnects to the Jumper Wires (This is only if you are using the non jumper version of the Arduino).
Example of what this looks like:
http://imgur.com/a/hJ4J2
IMPORTANT: Add a 1k Resistor going from the Logic Controller 3.3v line to the 3.3v data line
This is to pull up the line to ensure no floating voltages or nothing like that.  You will run into problems if you do not follow this step.
This step will be repeated multiple times because it can be overlooked and will cause problems



# Part 3 - Wiring the Circuit:
You are going to have to install the Nicohood Library linked above.  He includes a tutorial on how to do that within his project page.

Download my Sketch that utilizes that library and upload it to your Arduino Mega 2560
This image details what wires will be used and what they are for.
http://imgur.com/HSHZKiw
This will be the pinout of everything.  Use the code for reference along with this guide
http://www.int03.co.uk/crema/hardware/gamecube/gc-control.htm
(This guide is super useful and should be used along the way)
Wire up all the matching pieces.  

Use this for picture reference http://imgur.com/LoOGKa7

The 5v (Yellow) line of the Gamecube controller cord will be used to power the Arduino.  
The 5v (Yellow) and 3.3v (Blue) line of the Gamecube controller cord must also power the Logic Controller in their respective spots (Hv for 5v and Lv for 3.3v).
White, Green, and Black all share a common ground, make sure you also ground the Arduino and Logic Controller to these wires.  

The Data line on Pin 8 of the Arduino Mega  will be 5 volts and will be attached to the Bidirectional Data Line of the Logic Controller which will then convert the 5v to 3.3v so you don’t overload your Gamecube.  Attach the opposing 3.3v side to the Gamecube controller (Red) Data Line
Make sure you have 1k Ohm Resistor going from the 3.3v line to the 3.3v data line 
Wire the Sanwa Buttons to the Desired Spots
They will share a common ground on one end and then the designated data line on the other side

Example of Wiring the A and Start Button
http://imgur.com/coZq3vI

After that you should be pretty much done!  I know this tutorial might have been super complicated but please just ask for any help and I would be glad to help out!




# Part 4 - Side Notes
I’ll include more stuff in future updates

I recommend looking at other people's fightstick ideas to get some ideas about building and constructing a box for this project and how to do it.
I purchased my stuff from Amazon and Focus Attack

Any Arduino 2560 will work including third party products.  If you want to support the Original company go ahead and buy theirs, but you will have to pay triple.  Also there is no pro mini version of the Mega 2560 so you will be stuck with the Jumpers

These are non-affiliate links of some stuff that I bought
Logic Controller
https://www.amazon.com/gp/product/B0148BLZGE/
Heat Shrink Kit
https://www.amazon.com/gp/product/B00OZSL8UE/
OBSF-24mm Sanwa Buttons.  OBSC-24mm for X, Y
https://www.focusattack.com/pushbuttons/popular-brands/sanwa/
(my referral link if you want to support me :) )
http://focusattack.com/?lr=59a8522fef0fb0f51904ab0f/
Wiring with Quick Disconnects already attached
This saves a load of time I bought 22 Gauge .110 connectors
The Daisy Chain ground 30 Ct  + Wire for Quick Disconnect
https://www.focusattack.com/electrical/wiring/by-size/
Lexan and Wood from Home Depot
Acrylic cracks easily and I do not recommend it (unless laser cutting).  A 12”x24” piece of Lexan cost about 15 dollars and is well worth the upgrade.
I used 1.5”x0.75” wood around the sides and ⅛” Plywood as the top and bottom cover.
I coat the wood in shellac to protect it from any damages.
Let me know if you want anymore links of any stuff I bought and I’ll include it!
When drilling your Acrylic or Lexan (I used a 15/16” Spade bit), and let the drill do the work and make sure you have a piece of wood underneath so you don’t get any pressure cracks.  (If drilling Acrylic I heard drilling in reverse can reduce cracking but do this at your own risk)
Here are some internal pictures of what mines currently looks like.  This is a fully working version one and I included a picture of the Arduino Mega Pro mini which is what I will be working with next.  When I am upgrading to the Mega Pro I’ll make a video tutorial on it!
http://imgur.com/a/l3JvO

This is the guide/print out for button placement: goo.gl/rT3BNP (drill only the 
buttons you need/want, add me on discord if you need a different layout simple#4286)


# Part 5 - Credits!
Nicohood!!  -  https://github.com/NicoHood/Nintendo
Along with the sources he credited in his project
I used his Multi-Single Player mod as the basecode of the project and built off of there.
This guide.  Honestly one of the most helpful resources I used.
http://www.int03.co.uk/crema/hardware/gamecube/gc-control.htm
GCForever
In particular user meneerbeer for the idea of eliminating the Gamecube controller completely and making it completely digital.
(My original idea involved a bunch of resistors and logic)
Dad and some friends :D
PracticalTAS and Gravy for the correct values of X1, X2, X3, Y1, etc.
Link to those values.  You can use this to fine tune your Box if the angles are off and you want them Exact.  For my case everything was 100% accurate :D
https://www.reddit.com/r/SSBM/comments/5g63al/smashbox_keyboard_emulation/daqqbhr/
Hitbox obviously for the idea of the whole Smash Box.
Random Sources on the internet that I will include if I remember. 

My finished product: http://imgur.com/a/kQsMd
This is how my recent boxes have been turning out: http://imgur.com/a/SfTXl



Just a small self plug! Thank you so much!!
If you enjoyed this guide and wish to support me my donation link is: 
paypal.me/SimpleControllers
Or
Just drop me a sub on Youtube or Twitter follow!
https://www.youtube.com/channel/UCvAvA7YGmhKn4KGXHKSvkMA
https://twitter.com/ssbmsimple




# Checklist!
(Print this out if you need to!!)

## Items you need:
Arduino Mega 2560
21 Sanwa Buttons 24mm OSBF/OSBC
Logic Controller 5v - 3.3v Bidirectional
1k Resistor for Logic Controller
Build 16”x8”x2” box or desired dimensions
15/16” Spade Bit to drill holes in box
Wires with quick disconnects .110”
Jumper wires (If you are running the non pro version of Arduino Mega)
Heatshrink + Solder/Soldering Iron
On Off switch if you want to toggle DPad
Something to Alleviate Cable Stress so if cable is pulled the stress is not put on Solder Points.  IE: A Zip Tie or something similar

## Wiring/Setup:
Add 21 Sanwa Buttons OSBF/OSBC to Box/Case
Optional Add On/Off button/switch for X/Y Tilt | Dpad Toggle
Use 15/16” Spade Bit for holes - Layout Here (goo.gl/rT3BNP)
Install Nicohood Library
Upload my sketch to Arduino Mega 2560
Splice Wires for Quick Disconnects/Jumper Cables
http://imgur.com/a/hJ4J2
Wire up the Gamecube Controller Cable to Logic Converter and Arduino Mega 
Use this guide for help! http://imgur.com/LoOGKa7
1k Resistor on Logic Controller going from 3.3v Power to 3.3v Data Line
Wire up the quick disconnect jumper cables to desired spots
Each Sanwa button has the Daisy Chained ground, and then a data wire going to the Arduino
Reference code for button spots 
A = 22
B = 24
And so on! You can use this if you can’t understand code well
http://imgur.com/HSHZKiw
Give it a quick test to make sure everything is working!
     End Result should look a little something like this!
http://imgur.com/a/l3JvO
Close up the box and you’re done!

Thanks for reading my guide and all the support!
