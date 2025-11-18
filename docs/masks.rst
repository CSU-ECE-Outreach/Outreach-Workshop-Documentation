Masquerade Masks
=================

Introduction
--------------------
In this workshop, we will be learning how to use neopixels to create colorful masks!


RGB or Red Green Blue
~~~~~~~~~~~~~~~~~~~~~~~
For this workshop, we will learn how computers see color! 

One way computers see color is by breaking down each pixel into its red, green, and blue components.

`For later: pick out some cool colors at this website: `

https://www.w3schools.com/colors/colors_picker.asp

What are neopixels?
~~~~~~~~~~~~~~~~~~~~

* Neopixels are special LEDs (Light Emitting Diodes) that can be used in strands to create cool sequences of colors
* They take RGB color values, and turn them into light!

`strip.color(<Red>, <Green>, <Blue>)`

Materials Needed:
------------------
1x Arduino Nano

1x Battery Cable

1x LED String

1x 9V Battery

Code 
-------------------
To make cool sequences, we will first begin with some starter code to copy in

Make sure you install Adafruit_NeoPixel before writing your code


.. code-block:: cpp

    // ---------------------------
    // Masquerade Workshop Code
    // Created by Joey Reback
    // Date: 11/17/2025
    
    // Set Arduino Library Pin Numbers and Number of LEDS
    #include <Adafruit_NeoPixel.h>

    #define PIN 6
    #define NUM_LEDS 6

    // Define LED Strip information
    Adafruit_NeoPixel strip(NUM_LEDS, PIN, NEO_GRB + NEO_KHZ800);

    // Leave this space below empty for your functions!


    // End of empty space

    // Initialize your LED Strip
    void setup() {
        strip.begin();
        strip.show();
    }

    // What Arduino will run in a loop
    void loop() {

    }


Theater Chase
-------------
Watch a color bounce back and forth!

.. code-block:: cpp

    //copy this part to your empty space
    void theaterChase(uint32_t c, int wait) {
        for (int j = 0; j < 10; j++) {
            for (int q = 0; q < 3; q++) {
                for (int i = 0; i < strip.numPixels(); i += 3) {
                    strip.setPixelColor(i + q, c);
                }
                strip.show();
                delay(wait);
                for (int i = 0; i < strip.numPixels(); i += 3) {
                    strip.setPixelColor(i + q, 0);
                }
            }
        }
    }

    //copy this line in void loop()
    // Replace <RED>, <GREEN>, <BLUE>, <TIME> with what you want
    theaterChase(strip.Color(<RED>, <GREEN>, <BLUE>), <TIME>);

Rainbow Cycle
---------------
Show all the colors of the rainbow!

.. code-block:: cpp

    //copy this part to your empty space
    void rainbowCycle(int wait) {
        for (long j = 0; j < 256 * 5; j++) {
            for (int i = 0; i < strip.numPixels(); i++) {
            strip.setPixelColor(i, Wheel((i * 256 / strip.numPixels() + j) & 255));
            }
            strip.show();
            delay(wait);
        }
    }

    //copy this line in void loop()
    // Replace <TIME> with what you want
    rainbowCycle(<TIME>);

Color Wipe
----------------
Show a color and then wipe it off!

.. code-block:: cpp

    // copy this part to your empty space
    void colorWipe(uint32_t c, int wait) {
        for (int i = 0; i < strip.numPixels(); i++) {
            strip.setPixelColor(i, c);
            strip.show();
            delay(wait);
        }
    }

    // copy this line in void loop()
    // Replace <RED>, <GREEN>, <BLUE>, <TIME> with what you want
    colorWipe(strip.Color(<RED>, <GREEN>, <BLUE>), <TIME>);

Color Fade
---------------
Fade between two colors!

.. code-block:: cpp

    // copy this part to your empty space
    void colorFade(uint32_t c1, uint32_t c2, int duration_ms) {
        uint8_t r1 = (c1 >> 16) & 0xFF, g1 = (c1 >> 8) & 0xFF, b1 = c1 & 0xFF;
        uint8_t r2 = (c2 >> 16) & 0xFF, g2 = (c2 >> 8) & 0xFF, b2 = c2 & 0xFF;

        for (int step = 0; step <= 100; step++) {
            float t = step / 100.0;
            uint8_t r = r1 + (r2 - r1) * t;
            uint8_t g = g1 + (g2 - g1) * t;
            uint8_t b = b1 + (b2 - b1) * t;

            uint32_t c = strip.Color(r, g, b);
            for (int i = 0; i < strip.numPixels(); i++) strip.setPixelColor(i, c);
            strip.show();
            delay(duration_ms / 100);
        }
    }

    // copy this line into void loop()
    // Replace <RED 1>, <GREEN 1>, <BLUE 1>, <RED 2>, <BLUE 2>, <GREEN 2>, <TIME>
    colorFade(strip.Color(<RED 1>, <GREEN 1>, <BLUE 1>), strip.Color(<RED 2>, <GREEN 2>, <BLUE 2>), <TIME>);


Assembly
--------------

MAKE SURE YOU DOUBLE CHECK YOUR WIRING !!

Plug in your LED Strip like this:

* GREEN -> D6
* RED -> 3V3
* WHITE -> GND

Plug your Battery Cable Like this: 

* RED -> VIN
* BLACK -> GND
(they should be right next to each other)

Running the Code
-----------------

To write your code to your arduino, click the (->) button in arduino IDE and wait a bit.

In a second, your LED strip should light up!

Writing your Own functions
----------------------------
If you finish early, try writing your own functions! If you need help getting started, ask a volunteer for help

Tip Code Segments:

Specify a specific color:
`uint32_t c = strip.Color(r, g, b);`

Set your pixel color: 
`strip.setPixelColor(i, c)`

Show your pixel color:
`strip.show()`

Delay function in arduino:
`delay(time)`

