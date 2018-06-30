Once you have your case modified, and your electronics tested, it's time for assembly.

# Front Assembly

### Components
* Front Case (pre-modified)
* Case screws
* Buttons (A/B/X/Y/Start/Select/Arrows)
* Silicone Membranes
* 3D Printed LCD Bracket
* 3D Printed Speaker Retainer
* LCD Screen Lens
* LCD
* Circuit Sword PCB.
* Speaker 

### Tools & Materials
* Nice 000 screwdriver like a Wiha 261/PM
* Kapton tape, 1/2" diameter is good.
* 2-part epoxy (Like clear gorilla glue epoxy) or Hot glue
* Tissue tape from DMG plastic screen protector

**Note:** You'll want to glue your front bracket down to secure the mounting posts for the rear case, there are only 6 screws holding the shell together, and four of them have been removed to make room for the larger LCD, so you must provide additional reinforcement to enable a solid final assembly.

I used Gorilla Epoxy Clear, because it's a structural epoxy ok for ABS and PET, you could use hot-glue but I would be very cautious tightening screws on final steps.

## LCD Bracket

Pop your LCD in the 3D printed bracket, place it in the case and dab your glue of choice in the areas highlighted, these are just suggestions to ensure you don't cause interference with the CS PCB, feel free to go wild and let us know what works by updating the wiki.

**Tip:** To prevent dust and fingerprints before lens application, you can leave the screen protector on the LCD: dog-ear the screen protector removal tab and tape it to the middle with a little bit of kapton, so you can reach it after the bracket is glued. Be careful when removing you don't tear the protector leaving strips under the bezel.

If you're using epoxy I'd advise you to clamp the assembly overnight, you can clamp 30 minutes and complete assembly if you're impatient, but to allow everything to fully set up: give it overnight. It "sets" in 5 minutes but it doesn't cure solid for 24 hours.

Remove the LCD screen protector, clear any dust, and affix the screen lens.

## Front Button & Mainboard PCB

With the front cover set and secure with your bracket and LCD installed, pop in your buttons and membranes, then connect the LCD header, lay the PCB down, if you get interference, check to make sure you made adequate relief for the USB-C connector.

Secure the CS Mainboard PCB using the screws from your case.

**Tip:** Some of the holes are oversized, use the somewhat larger screws from the metal plate where the smallest screws wont grab plastic.

**Important Note:** Cover the USB-C connector in two layers of Kapton to prevent activation of the Mode switch installed just above it in the rear of the case.

## Speaker

Solder up your speaker wires, run them out the channel in the speaker well, press fit the retainer over the speaker and plug in the connector. 

## Fan Duct
Cut strips of the tissue tape that comes with the cheap DMG screen protector to secure the fan to the bracket on the posts.

Place 3M VHB tape in this configuration on the CM3 module, the strips on the PCB are doubled-up, the strip on the DIMM socket is single thickness.

Plug in the fan first, then place the duct like so, route the fan cable so it doesn't get pinched, I used a loop of Kapton secured to the "back" to secure it to the duct.

That VHB is tenacious stuff, so be affirmative with your placement and don't futz around with it.

# Rear Assembly

### Components
* Rear Case (pre-modified)
* Case Screws
* Buttons (L1/L2)
* Power Switch
* Modified Silicones for Button Bracket (trimmed to circles)
* 3D Printed Button Bracket
* 3D Printed Support Bracket
* 3D Printed Power/Mode Support
* 3D Printed Back Board Support
* 3D Printed Duct Plate
* Back Button Board
* Back Board (Analog Volume or Mini HDMI)
* Back Board ribbon cable
* Wiring Harness for analog volume (if needed)
* Wiring Harness for Mode/Power/L1/L2
* Wiring Harness for speaker
* Speaker

### Tools & Materials
* Hole punch
* Kapton Tape
* Soldering Iron
* Wire Cutters
* Wire Strippers
* Nice 000 screwdriver like a Wiha 261/PM 

Back case is not difficult, it's the only soldering you'll need to do.

# Rear Case Electronics Prep

## Back Buttons
First, solder up the Back Button PCB, you only need ground and whatever buttons you require.  Once wired up, plug in the other end to the mode/power board.

**Tip:** If using only two rear buttons, you may utilize *either* header on the CS board, you don't need to use both. In other words, you can wire up L1/R1 to L1/L2 header and it doesn't matter, saves some wiring since L and R shoulder pairs terminate on two different headers.

## Mode/Power
Place the provided mode button tact switch in place on the 3D printed support, install the harness connector now if you haven't already, just to prevent fiddling with the part later. Place the mode/power board on the support block and secure it using two screws, place it in the case and align the button before soldering, and make sure to **trim the leads afterwards**.

**Important Note:** After trimming the mode button leads flush with the PCB, cover the pads with Kapton to prevent contact with the USB-C connector, which will cause errant activation of the mode button.

## Back Board

Place the Back Button Support next to the upper right mounting post, install the appropriate Back Board for your installation and secure it with a screw to the block, you have some room to fine-tune placement.

At this point you should have the Back Board Support, Power Board Support, and Fan Duct Plate ready to go, but we need to secure all this stuff in place.

# Rear Case Assembly

## Fan Duct

Secure the fan duct plate using four screws.

## Rear (L1/R1, L2/R2) Buttons

Pop the back button bracket in, pop the buttons in.

Take the cheap DMG style plastic screen protector that came with your case and punch out a couple little circles with the hole punch, jam these in the undersides of the buttons to reduce travel.

Pop in some membranes cut to circles.

Place the Back Button PCB on the membranes, then place the Back Button Board Support, secure the left side only.

## Back Board

Install the ribbon connector in the Back Board now, Place the Back Board in the rear case and secure the right side of the Back Button Board Support through the Back Board.

## Mode Power Board

Place the Mode/Power assembly in place with the external power switch plastics, if it's not situated already.

At this point you should have the Mode/Power board secured and connected, the Back Board secure to the 3D printed block and to the Back Button Board Support, and your buttons installed and retained with the Back Button Board Support Bracket, as well as the Fan Duct Plate installed.

You are ready for Final Assembly.

## Final Assembly

### Components
* Battery (with JST-PH Header)
* Large Case Screws (x6)
* Battery Cover
* Random Cartridge


### Optional
* 2x M2 Washers to reinforce cheap case molding

Connect the Back Board ribbon cable to the Circuit Sword PCB.

Close up the case, secure with the six larger self tapping screws included with your case.

**Tip:** The holes in the case are barely smaller than the heads on the provided screws and may threaded its way through the plastic with little force, to address this: insert an M2 washer into the well from the rear.

Connect up the battery. **You did confirm polarity right???**

**Tip: Be careful if you use tweezers you don't short the battery!**

Pop in a cartridge, there should be no interference.

Seriously, that's it, fire it up.