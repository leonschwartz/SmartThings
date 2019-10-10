# SmartThings
Home automation through SmartThings is one of the things that make the 21st century great.  This repo contains some of the device handlers and smart apps I've hacked together that I think might be useful to others.

# Nightlights
I originally wrote this code when my in-laws were looking for something brighter than the traditional plug-in nightlights which did not provide enough light.  Since then, I've used these to keep the lights on (and very dim) for my kid.  With the right z-wave dimmer (I have handlers for both the Leviton DZ6HD and the GE z-wave dimmers, but the Leviton provides much better functionality due to having better firmware), you can have a switch that operates like a normal swith during the day, but then automatically turns on and/or dims to your preset level, triggered by whatever event you wish (such as typical bedtime, but you can use your imagination here).  In the morning, the lights automatically turn off.  If you try to turn the nightlights off at night, they will not (unless you use a slave switch, in which case they might, but go right back on).  You can make the lights brighter when in nightlight mode through the dimmer switch or the app, and when turned off, they return to dimmed status.  GE switches have some drawbacks -- main one is that in the morning, the lights have to ramp up to full bright and then turn off (otherwise the next time you use the switch, they will turn on to dimmed level) -- limitation of GE firmware, unfortunately.

You need the device handler and the smart app, though you can manually put any dimmer into nightlight mode from the device handler code itself; the smart app ties this into grouping them and event-catching.

# License
The code is based on existing Apache-licensed code (see comments in code) and remains under the Apache License v2.0.
