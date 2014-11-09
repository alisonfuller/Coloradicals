Coloradicals
===========
Background/Introduction/Client Information

  In recent years, there has been a surge in the interest in personal health and food quality. Accompaning these new interest there has been a dramatic increase in local and urban farms. The problem arises when the smaller farms try to compete with the production and prices of larger specialized farms. Our goal for a project is to help smaller scale, local farmers increase efficiency without dramatically increasing cost. Our client is Jacob Spring's Farm but we will also be attempting to aid the population smaller-scaled farmer. In order to accomplish this goal, our team is specifically addressing ventilation systems in greenhouses. Greenhouses must be kept at certain conditions year around in order to optimize production. There are currently products on the market that automate ventilation, but these products are too expensive for smaller scale farmers to afford.

Design Requirements

  The requirements for our project include the arduino uno, a temperature sensor, a motor, and a power source. The arduino allows us to be able to configure our project that helps our client the most and control the different parts we attach in an effective way. One of the most important parts of setting up our arduino is making sure that it has enough power to give out to the different parts we are controlling whether that be the temperature sensor, motor, or other addons we consider. For example, our motor uses a lot of power and requires a second battery to be able to run which needs to be taken account of when making our project. Our temperature sensor is a requirement because it tells our arduino when it needs to send a signal to control the motor. The temperature sensor must be able to determine when the temperature inside the greenhouse hits below or above our clients desired temperatures otherwise our product wouldn't be usable. For example, a common temperature range for greenhouses is between 50 degrees fahrenheit and 68 degrees fahrenheit and our sensors would just need to be able that when the indoor temperature is not in this range it must send a message to the arduino to start the motor. The final design requirement is the motor and it is reliant on the other two requirements to be able to function, but is still necessary for the success of our project. The motor is used to control the vents in the greenhouse so that the inside can be kept at a consistent and safe temperature. Finally we have to have a power source that is powerful enough to keep our project running for long periods of time without problems.
  
Design Alternatives
  
  For our project, our team has considered many different alternatives. In our brainstorming, we considered both solar and battery options as a power source for our device. We have also dicussed adding more sensors such as a carbon dioxide and humidity sensor in order to give the device more functionality. Regarding the component that causes the vents to open and close we have thought of a few options. The first option was to have a wheel attached to the motor with an arm attached to it, also attached to the bar along the vent shades, that would be able to open and close the ents as long as the motor was able to move in two directions (clockwise and counterclockwise). Another option would be to use a motor that moves a track with gears forwards and backwards that would be attached to the bar along the vent shades. For our final option we thought of two motors that used a pulley system to move the vents, with the motors only moving in one direction each. Each motor would either pull the vents closed or open them. Next, we considered incorporating a component that would be able to send the client notifications through an app or text message in order to alert the client when the temperature is above or below the set temperature parameters so the client can manually open or close the vents. There are different kinds of motors that we could use for some of the options in order to move the vent shades. One option is to use a step motor that would be able to move in increments of 1.8 degress per pulse, giving precise aounts of movement. Another option would be to use a gear motor that would have more torque than other motors, but would need to have a set time that the motor runs rather than a specific amount of degrees that it isrotated. Our last consideration was to either use our client's existing vent and adapt our device to control it, or use another vent and replace the existing one. If we are to use a new vent our device would be able to be more compatible with the new vent.
  
Budget and Bill Of Materials
  
  *We just need to pull this information from our slide show*
  
Timeline

  *this can also be adapted from what we already have*
  
Appendix

  Code: Curently we have a code that turns a motor on and off in response to temperature as well as a code for our servo motor. For our final project these codes will be combined and altered.
  
    Temperature Changing Code:

    #include <LiquidCrystal.h>

int tempPin = 0;
int lightPin = 1;
int motorPin = 13;

//                BS  E  D4 D5  D6 D7
LiquidCrystal lcd(7, 8, 9, 10, 11, 12);

void setup() 
{
  lcd.begin(16, 2);
  pinMode(motorPin, OUTPUT);
}

void loop()
{
  // Display Temperature in C
  int tempReading = analogRead(tempPin);
  float tempVolts = tempReading * 5.0 / 1024.0;
  float tempC = (tempVolts - 0.5) * 100.0;
  float tempF = tempC * 9.0 / 5.0 + 32.0;
  //         ----------------
  lcd.print("Temp        F  ");
  lcd.setCursor(6, 0);
  lcd.print(tempF);
  
  // Display Light on second row
  int lightReading = analogRead(lightPin);
  lcd.setCursor(0, 1);
  //         ----------------
  lcd.print("Light           ");  
  lcd.setCursor(6, 1);
  lcd.print(lightReading);
  delay(500);
  if (tempF < 70){
   // digitalWrite(LEDpin, HIGH);
   digitalWrite(motorPin, HIGH);
   delay(250);
 }
   else{ 
//digitalWrite(LEDpin, LOW);
digitalWrite(motorPin, LOW);
}
}

  Servo Code:
      // Sweep
// by BARRAGAN <http://barraganstudio.com> 
// This example code is in the public domain.


    #include <Servo.h> 
 
Servo myservo;  // create servo object to control a servo 
                // a maximum of eight servo objects can be created 
 
int pos = 0;    // variable to store the servo position 
 
void setup() 
{ 
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object 
} 
 
 
void loop() 
{ 
  for(pos = 0; pos < 90; pos += 1)  // goes from 0 degrees to 180 degrees 
  {                                  // in steps of 1 degree 
    myservo.write(pos);              // tell servo to go to position in variable 'pos' 
    delay(15);                       // waits 15ms for the servo to reach the position 
  } 
  for(pos = 90; pos>=1; pos-=1)     // goes from 180 degrees to 0 degrees 
  {                                
    myservo.write(pos);              // tell servo to go to position in variable 'pos' 
    delay(15);                       // waits 15ms for the servo to reach the position 
  } 
}


  
