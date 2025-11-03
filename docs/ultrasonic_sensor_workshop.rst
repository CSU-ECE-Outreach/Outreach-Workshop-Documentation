Ultrasonic Sensor Workshop
================================
Introduction
--------------------
In this workshop we will be learning about these components:

* Ultrasonic Sensor
* Buzzer
* RGB LEDs
* Arduino
* Breadboard

So pay attention to the slides to learn about how these components work!

Wiring Up the Circuit
--------------------
Here's the circuit diagram for setting up the ultrasonic sensor with an Arduino:

    .. figure :: images-ultrasonic/ultrasonic_circuit_diagram.png
        :alt: Circuit diagram for ultrasonic sensor workshop
        :align: center

        Circuit Diagram for Ultrasonic Sensor with Arduino

Code
--------------------
Here's the code you'll be working with during the workshop:

.. code-block:: cpp

    // ---------------------------------------------------------------- //
    //  Arduino Distance Classification Using Ultrasonic Sensor 
    //
    //  Date: 10/28/2022
    //
    //  Author: Brayan Trejo
    //  Email:  brayan.trejo@colostate.edu
    //
    //  Department of Electrical and Computer Engineering 
    //  Colorado State University 
    //
    //  Revised 11/1/2023 with suggestions from Ross and Fatimah
    // ---------------------------------------------------------------- //


    // Define Arduino Pinout connections
    #define PIN_ECHO 2          // Connect Arduino pin 2 ---> Echo pin of Ultrasonic Sensor
    #define PIN_TRIG 3          // Connect Arduino pin 3 ---> Trig pin of Ultrasonic Sensor

    #define PIN_BUZZER 11        // Connect Arduino pin 11 ---> Positive terminal of Buzzer. Fun fact- certain pins have PWM capabilities.
    #define PIN_GREEN_LED 5     // Connect Arduino pin 5 ---> Positive terminal of Green LED 
    #define PIN_BLUE_LED 6      // Connect Arduino pin 6 ---> Positive terminal of Blue LED 
    #define PIN_RED_LED 7       // Connect Arduino pin 7 ---> Positive terminal of Red LED 


    // Define variables used for calculating and classifying distance 
    double duration;        // Variable for the duration of sound wave round-trip travel
    double distance;        // Variable for the distance measurement

    // ***TO DO***: ENTER THRESHOLD VALUES (in centimeters), MAXIMUM VALUE = 50
    int long_range = ;      // Variable that sets maximum detection distance 
    int mid_range = ;       // Variable that sets mid-range detection distance 
    int close_range = ;     // Variable that sets close-range detection distance 


    // ***TO DO***: Setup code. Runs only one time.Setup the respective pins to be either Outputs or Inputs. 
    void setup() {   
        pinMode(PIN_TRIG, );           // Sets the Trig Pin as an OUTPUT
        pinMode(PIN_ECHO, );            // Sets the Echo Pin as an INPUT
        pinMode(PIN_BUZZER, );         // Sets the Buzzer Pin as an OUTPUT
        pinMode(PIN_RED_LED, );        // Sets the Red LED Pin as an OUTPUT
        pinMode(PIN_BLUE_LED, );       // Sets the Blue LED Pin as an OUTPUT
        pinMode(PIN_GREEN_LED, );      // Sets the Green LED Pin as an OUTPUT
        Serial.begin(9600);                  // Starts the serial communication with the PC 
        Serial.println("Distance Classification System With Arduino Uno R3");  // Prints text to the serial monitor

    }


    // MAIN CODE: RUNS REPEATEDLY
    void loop() { 
        distance = get_Distance();
        classify_Distance(distance);
        delay(5);
    }


To Do
---------------------

We want these colors to light up from these ranges:
    .. figure :: images-ultrasonic/ultrasonic_range.png
        :alt: Distance ranges for ultrasonic sensor workshop
        :align: center

        Distance Ranges for LED Indications

1. Define threshold values for long_range, mid_range, and close_range in centimeters (max 50 cm).
2. Complete the setup() function by specifying which pins are INPUTS and which are OUTPUTS.

Breadboard Help
--------------------
If you're new to using a breadboard, here are some tips:

Below is a picture of how a breadboard works:

    .. figure :: images-ultrasonic/breadboard.jpg
        :alt: Breadboard wiring for ultrasonic sensor workshop
        :align: center

        Courtesy of DigiKey: Breadboard Wiring Example

Each vertical column of holes on the sides are connected internally. The middle section is split in half, so the left and right sides are not connected. Use this to your advantage when wiring up your components!

Bonus Challenges
---------------------
1. Modify the code so that you can display colors other than just red, green and blue. Like purple, yellow, cyan, and white.

.. code-block:: cpp

   // Example: To create yellow, turn on both red and green LEDs
   digitalWrite(PIN_RED_LED, HIGH);
   digitalWrite(PIN_GREEN_LED, HIGH);
   digitalWrite(PIN_BLUE_LED, LOW);

2. Add functionality to the buzzer so that it beeps at different rates depending on the distance range detected.

.. code-block:: cpp

    // Example: make buzzer beep at different pitches:
    
    // put this before the setup() function
    int frequency = 1000; // Frequency in Hz

    // put this inside classify_Distance() function
    tone(PIN_BUZZER, frequency); // frequency in Hz
