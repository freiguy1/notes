## High Tech Mailbox

> My notes for the high tech mailbox built for receiving cards at Kaytee and Ethan's wedding reception and also wowing guests.

-----------

This mailbox will be interactive in that it will respond with certain actions when triggers are pulled.  Currently I'm thinking trigger number `1` would prompt action `1` and trigger `2` would prompt action `2`.

**Ideas for triggers**

1. Detect a card being inserted using an infrared LED and detector.  When the light plane is broken, something is being inserted.
2. Detect when the door opens and closes. This will be done using a [magnetic door switch](https://www.sparkfun.com/products/13247).

**Ideas for mailbox actions**

1. Raise a flag on the side. Lower it then after a duration has passed.
2. Slowly brighten some interior LEDs. Dim them after a duration has passed.
    - Perhaps make the LEDs have a different color every time.

**Electronic Materials (to buy)**

- 1 [infrared LED emitter and detector](https://www.sparkfun.com/products/241)
- 1 [microcontroller](https://www.sparkfun.com/products/11232)
- 1 [(2?) diffused RGB LEDs](https://www.sparkfun.com/products/10821) (common anode means the power can be supplied straight from the power supply, so L7805 -> anode -> resistor -> PWM)
- 1 [magnetic door switch](https://www.sparkfun.com/products/13247)

**Hardware Materials**

- 5 6' 1x6 pine boards
- 1 drawer magnet
- 2 hinges for roof
- 2 hinges for door
- 1 door handle
- 1 mailbox flag
- 1 bottle of wood glue
- assortment of sandpaper
- preferred paint or stain


#### Digital plans!

**Pin Configuration**

- Infrared Detector: PCINT0 (PA0)
- Door Detector: PCINT1 (PA1)
- Red PWM: OC0A (PB2)
- Green PWM: OC0B (PA7)
- Blue PWM: OC1A (PA6)
- Servo PWM: OC1B (PA5)

