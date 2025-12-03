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