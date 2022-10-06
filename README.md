# Arduino_servo_test1

#include <Servo.h>
#include <ServoEasing.h>
#include <AccelStepper.h>

Servo servo1;

int PINSERVO = 2;
int PULSOMIN = 500;
int PULSOMAX = 2500;

void setup(){
servo1.attach(PINSERVO, PULSOMIN, PULSOMAX);
}

void loop(){
servo1.write(0);
servo1.setSpeed(550);

delay(1000);
servo1.write(90);
delay(2000);
servo1.write(180);
delay(1000);
}
