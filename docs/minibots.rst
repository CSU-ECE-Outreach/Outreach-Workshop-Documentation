Minibots Workshop
=======================

Wiring
-------------------
.. figure :: images-minibots/minibots-insts-1.png
        :alt: Wiring the minibots
        :align: center

Code
-------------------
.. code-block:: cpp

    #include <AFMotor.h>
    AF_DCMotor R_motor(2); // defines Right motor connector
    AF_DCMotor L_motor(1); // defines Left motor connector

    void setup() {

        Serial.begin(9600); // sets up Serial library at 9600 bps
        pinMode(A5, INPUT); // Sensor pin
        //***Set your motor speed. A good start speed is 200. Between 80 (min)-255 (max), and must be an even number.
        L_motor.setSpeed(220); // sets L motor speed
        R_motor.setSpeed(220); // sets R motor speed
    }

    void loop() {
        while (digitalRead(A5) == LOW){ // while it senses
            //***Optional: Mess around with these numbers. What do you notice about how the robot moves?
            rightTurn(1300); // turn right
        }
        forward(10); 
    }

    void forward(int delayNum){
        L_motor.run(FORWARD); // moves motor L Forward
        R_motor.run(FORWARD); // moves motor R Forward
        delay(delayNum); // move forward for 2 secconds
    }

    void rightTurn(int delayNum){
        R_motor.run(BACKWARD); // moves motor R Backwards
        delay(delayNum); // turns right
    }



Uploading
-------------------
.. figure :: images-minibots/minibots-insts-2.png
        :alt: Uploading to the minibots
        :align: center


Code Breakdown for Curious Folk:
----------------------------------
* Sets pin A5 as an input pin, likely for reading from a sensor (e.g., an obstacle detection sensor).
* Motor Speed Setup: The motor speed is set to a certain value
* ``digitalRead(A5) == LOW`` : Reads the state of pin A5. If the sensor detects a specific condition (LOW signal, such as an obstacle or line), the robot will turn right.
* ``rightTurn(1300);`` : Calls the rightTurn() function to turn the robot right. The argument 1300 determines how long the robot will turn.
* ``forward(10);`` : After the robot turns, it moves forward for a certain amount of time (10 milliseconds in this case).
* ``L_motor.run(FORWARD);`` and ``R_motor.run(FORWARD);``: Makes both the left and right motors move forward.
* ``delay(delayNum);``: Pauses the program for a specified time, determined by the delayNum argument. This controls how long the robot moves forward before executing the next action.
* ``R_motor.run(BACKWARD);``: Makes the right motor move in reverse. This causes the robot to pivot around the left motor, effectively turning it to the right.
* ``delay(delayNum);``: The robot will turn for the amount of time specified by the delayNum argument.