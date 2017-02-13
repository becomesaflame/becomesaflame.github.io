---
author: sgrandpre
comments: true
date: 2013-04-05 16:27:16+00:00
layout: post
link: https://sgrandpre.wordpress.com/2013/04/05/cooking-with-science/
slug: cooking-with-science
title: Cooking with Science!
wordpress_id: 115
categories:
- Electronics
- Things
tags:
- cooking
- PID
- sous vide
- temperature control
---

When I heard about sous-vide cooking, I knew I had to make one.  It's a way of producing perfectly cooked meat, and it involves messing around with electronics.  Right up my alley!   I decided to put one together for my girlfriend as a Christmas present.  She loves cooking, and making the project as a gift gave me a deadline and ensured I'd actually finish it.

Sous-vide cooking involves vacuum sealing food (usually meat) and cooking it in a temperature controlled water bath.  The idea is to set the water temperature to exactly what you want the internal temperature of your food to cook to, then leave it for a few hours.  It won't overcook or dry out.  Then you can take it out, sear the outside to make it crispy and brown, and have a thick, juicy steak that's cooked perfectly evenly medium rare straight through.

I decided to make a temperature controller that would switch power to an off-the-shelf crockpot.  I bought a thermocouple and a PID temperature controller with an autotune function and rigged up a proof of concept with a rice cooker from a thrift store.  I configured the PID controller to use the built-in relay and spliced it into the power cord of the rice cooker, and dangled the thermocouple into the water in the rice cooker.  It took a long time to get it running.  The thermocouple had three leads, two blue and one red.  I couldn't find any description of which lead was which.  Most thermocouples only have two leads.  I eventually figured out that the two leads that were the same color should go to the + and - pins, and the odd lead should go to the R pin, but the setup still wouldn't work.  I eventually replaced the thermocouple and it worked fine - the first one must have been either damaged in shipping or possibly fried when I hooked a multimeter up to try to determine which lead was which.  I never did figure out what the thermocouple labels on the PID controller meant, or why there was a third lead.  If anyone has an idea, let me know!

![](http://sgrandpre.files.wordpress.com/2013/03/photo-13.jpg)
<em style="text-align: center;">It took a while to figure out how to properly wire the thermocouple</em> 

Once I figured out the thermocouple setup, I bought some pre-sealed steak from Meat House in Arlington and tried out my bare-bones sous vide cooker.  I sat my rice cooker on a counter with the temperature controller spliced into its power cord and the thermocouple hanging into it.  I ran the auto tune function on the PID controller, set it 130 degrees F, and let it come up to temperature.  I threw in the sealed steak and left it for a couple hours, then pulled it out and seared it on the grill.  My setup may have looked like a couple components and a bunch of wires strewn across the counter, but it produced a damn good steak!

I found the clicking of the built-in relay on the PID controller to be pretty distracting, so I ordered a solid state relay to use on the final version.

I found a single power outlet with a built in switch at Home Depot that could provide both the outlet that the crockpot/rice cooker would plug into, and the power switch for the sous vide cooker.

![](http://sgrandpre.files.wordpress.com/2013/03/photo-2.jpg)
<em style="text-align: center;">Power switch and output outlet</em> 

Here is the wired up sous vide cooker with all the parts attached to the enclosure.  You can see the back of the output outlet/power switch, the solid state relay sitting on top of a large heat sink, and the PID controller.

![](http://sgrandpre.files.wordpress.com/2013/03/photo-6.jpg)
<em style="text-align: center;">All wired up!</em>

This is what the finished sous vide cooker looked like from the front.  Pretty slick!

![](http://sgrandpre.files.wordpress.com/2013/03/photo-3.jpg)
<em style="text-align: center;">Aww yissss</em>


### 




### Parts list:


[PID Temperature Controller](http://www.lightobject.com/JLD612-Dual-Display-PID-Temperature-Controller-P43.aspx)          $32.50
[Solid State Relay](http://www.lightobject.com/Search.aspx?k=ESSR-25DAC)                                  $8.50
[Heat sink for relay ](http://www.lightobject.com/Heat-sink-for-25A-SSR-P583.aspx)                              $4.25
[PT100 thermocouple ](http://www.lightobject.com/Premium-Stainless-Steel-Waterproof-PT100-RTD-Temperature-Sensor-Probe-Threaded-P681.aspx)                        $22.50
[Switch and Power outlet combo](http://www.homedepot.com/buy/leviton-15-amp-tamper-switch-and-outlet---white-r62-t5225-0ws.html#.UTJXKqUwlTs)    $7.99
Strain Reliefs
Enclosure


### Additional Resources:


[Guide to cooking with sous-vide](http://www.seriouseats.com/2010/03/how-to-sous-vide-steak.html)[
Cooking time and temperature reference
](http://www.sousvidesupreme.com/en-us/sousvide_cookingtemperatures.htm)
