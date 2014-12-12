Coloradicals
===========
![Team](https://cloud.githubusercontent.com/assets/8839851/5417617/61db715a-81f8-11e4-8228-b72a94213421.jpg)
# Abstract

The problem that we have been working to solve is that there are small farmers, such as our client Andre Houssney, that have to regulate the temperature in their greenhouses. Andre has to manually open and close his vents in order to control the temperature inside by allowing air to escape or enter the greenhouse. Andre has many tasks he has to do every day on his farm, and monitoring the temperature in his greenhouse and guessing when to open and close his vents is a task he would like to not have to worry about. We have made a solution to Andre’s problem, that could also be applied to other farms’ greenhouses to regulate the temperatures within the greenhouse. Our product is a device that reads the temperature within the greenhouse and will automatically open and close the vents to regulate the temperature. The user can set what temperature that they would like the greenhouse to stay at by adjusting the knob on the control panel, and the device will use a motor attached to the vent to open and close the vents. Our product is intended to automatically regulate the temperature within the greenhouse without any work to be done by the user.

# Background/Introduction/Client Information

  In recent years, there has been a surge in the interest in personal health and food quality. Accompaning these new interest there has been a dramatic increase in local and urban farms. The problem arises when the smaller farms try to compete with the production and prices of larger specialized farms. Our goal for a project is to help smaller scale, local farmers increase efficiency without dramatically increasing cost. Our client is Jacob Spring's Farm but we will also be attempting to aid the population smaller-scaled farmer. In order to accomplish this goal, our team is specifically addressing ventilation systems in greenhouses. Greenhouses must be kept at certain conditions year around in order to optimize production. There are currently products on the market that automate ventilation, but these products are too expensive for smaller scale farmers to afford.

# Design Requirements

  The requirements for our project include the arduino uno, a temperature sensor, a motor, and a power source. The arduino allows us to be able to configure our project that helps our client the most and control the different parts we attach in an effective way. One of the most important parts of setting up our arduino is making sure that it has enough power to give out to the different parts we are controlling whether that be the temperature sensor, motor, or other addons we consider. For example, our motor uses a lot of power and requires a second battery to be able to run which needs to be taken account of when making our project. Our temperature sensor is a requirement because it tells our arduino when it needs to send a signal to control the motor. The temperature sensor must be able to determine when the temperature inside the greenhouse hits below or above our clients desired temperatures otherwise our product wouldn't be usable. For example, a common temperature range for greenhouses is between 50 degrees fahrenheit and 68 degrees fahrenheit and our sensors would just need to be able that when the indoor temperature is not in this range it must send a message to the arduino to start the motor. The final design requirement is the motor and it is reliant on the other two requirements to be able to function, but is still necessary for the success of our project. The motor is used to control the vents in the greenhouse so that the inside can be kept at a consistent and safe temperature. Finally we have to have a power source that is powerful enough to keep our project running for long periods of time without problems.
  
# Design Alternatives
  
  For our project, our team has considered many different alternatives. In our brainstorming, we considered both solar and battery options as a power source for our device. We have also dicussed adding more sensors such as a carbon dioxide and humidity sensor in order to give the device more functionality. Regarding the component that causes the vents to open and close we have thought of a few options. The first option was to have a wheel attached to the motor with an arm attached to it, also attached to the bar along the vent shades, that would be able to open and close the vents as long as the motor was able to move in two directions (clockwise and counterclockwise). Another option would be to use a motor that moves a track with gears forwards and backwards that would be attached to the bar along the vent shades. For our final option we thought of two motors that used a pulley system to move the vents, with the motors only moving in one direction each. Each motor would either pull the vents closed or open them. Next, we considered incorporating a component that would be able to send the client notifications through an app or text message in order to alert the client when the temperature is above or below the set temperature parameters so the client can manually open or close the vents. There are different kinds of motors that we could use for some of the options in order to move the vent shades. One option is to use a step motor that would be able to move in increments of 1.8 degress per pulse, giving precise aounts of movement. Another option would be to use a gear motor that would have more torque than other motors, but would need to have a set time that the motor runs rather than a specific amount of degrees that it isrotated. Our last consideration was to either use our client's existing vent and adapt our device to control it, or use another vent and replace the existing one. If we are to use a new vent our device would be able to be more compatible with the new vent.
  
# Overview of Process
  
  When we chose to use a window shutter for our project, we were faced with the issue of the size of the shutter. We shortened the length of the shutter to 25 3/8", but we didn't change the width of the shutter, so it is still 20 3/8". In order to change the length of the shutter, we had to disassemble the entire set up, which required us to unscrew the hinges, 8 other screws. When we took the screws out, the siding came apart from the blinds themselves. We then had to measure the length of siding that we wanted, and decided on 25 3/8" for the length of the shutter. This allowed us to keep 6 individual blinds in the shutter. After we measured the length that we wanted, we took the disassembled shutter down to the manufacturing center to cut the siding. After we cut the siding, we lost two sets of the original holes that were needed to hold the shutter togheter. We then had to measure the location and diamter of the holes, and had to re-drill some new holes into the sides. Once we drilled the new holes, the reassembly of the shutter was easy. We just had to drill the screws back in and the shutter was completely reassembled. The next step was to mount the motor on the blinds so we could automate them. A servo motor was ideal for the blinds since we would be able to control the amount of degrees the motor will rotate, and there were single motors that would have enough power to move the blinds in both directions. To mount the motor we used a u-shaped piece of metal and cut it to fit to the vent. The brackett is screwed directly to the mounting holes already on the motor and screwed into the top of the vent. The motor is mounted right next to the bar that connects all of the vents together. On the motor there is an arm which is screwed into the side of the bar so that when the motor rotates it will cause all of the vents to move simultaneously. The motor is connected to an arduino board that will control, as well as power, the motor and will move based on the temperature parameters.
    
# Final Design

## Description

  The final design of our project consists of a plastic vent with a servo attachment that directly attaches to an LCD interface. The vent was modified in order to fulfill our clients’ dimensions. A temperature and humidity sensor is present inside the LCD box as well as a light sensor that peeks out the sides. The box LCD interface is easily mounted onto any structure that our client desires, but needs to be in close proximity to the vent. 
  The LCD screen displays four different items, current temperature, set temperature, humidity, and light. The set temperature on the LCD screen is altered by the user to turning a knob on the box to the desired temperature parameter. If the temperature of the Greenhouse falls below the user inputted temperature, the blinds close. If the temperature lies above the inputted temperature then the blinds will open. The servomotor is attached to the vent by a metal arm that allows for the blinds to open and close based on the parameter that is given. 
  Our circuit is encased in the box that also holds the LCD screen. Our power source is two 9-volt batteries. One of the batteries powers the arduino and sensors while the other one controls the servomotor and LCD screen. The batteries are easily accessed within the box and can be changed by our client as needed.

## Manufacturing
  
  The project was mainly code and circuiting intensive though other parts of our system needed to be altered. The plastic vents were altered from 48 inches long and 20 inches wide to 25 inches long by 20 inches wide. We also   needed to manufacture a metal arm that allowed the servo to open and close as the parameters change. 
  As far as the circuiting of the project, there were many challenges faced. Our circuit needed a lot of troubleshooting in order to make sure that there was not power where power shouldn’t be. There were capacitors, transistors, regulators, temperature, humidity, and light sensors, an LCD screen, as well as a servomotor attached to a single solder-able breadboard. 
  In order to make sure that the circuit board was protected, our group worked in the manufacturing center in order to alter a box in order for it to hold the LCD screen, knob, and circuit board. It was also important to make sure that the box made would be suitable for mounting in our clients Greenhouse.
  
# Testing and Analysis

   Our design had two critical parts, the mechanical aspect of the shutter and motor system along with the electrical and coding component. When designing the shutter and motor system, we consider several different types of sytems such as a pulley system and using a linear actuator. In our prototype, we designed a pulley system for our vent. This design ultimately fell short when testing and trying to move the shutter in two directions. With this in mind, team decided to design a system using a servo that would be able to move two directions with more ease. The process of picking a servo for our design required research and calculating the torque that would be applied to the servo. We measured the force to open the vent to be about 8.3 N and the approximate radius of a necessary arm to be around .05 meters. Knowing that the most torque would be applied to the servo when at 90 degrees, we calculated the torque to be around .425 Newton-meters based on the equation torque=(Force)(radius)sin(theta). The servo that we chose for our design allows for torque of 1.94 Newton-meters which allows for variance in vents for other models in the future. When testing our system with the servo, we found the vent was not moving as smoothly as desired. This lead to the creation of a small channel in the arm to allow for slight changes in the radius.
  There was also testing involved in the creation of our code and circuitry. In the early stages of the design process we used LED lights to check our coding and circuitry of the sensors and the LCD screen. With the integration of the servo and through hole bread board, we tested each connection with a voltameter and tested our system using the power supply. After testing with the power supply, we tested our system with batteries where we discovered that we needed to add more capacitors to account for the power of the servo.
  Once we had our entire system assembled, we tested our design by setting and checking different temperature settings and observing the adjustments of the vent. 
  
# Conclusion

  For our project we designed an automatic vent that would help regulate the temperature of a greenhouse. We made a vent and motor system that would be controlled by an arduino that we coded. The code and arduino were used to control the different aspects of our project ranging from the temperature sensor to the LED screen to the motor. All of these parts that the arduino controlled were stored inside of a box we manufactured to exactly match our needs. The way our project works is by detecting the temperature of the greenhouse and if it hits a set parameter it will cause the motor to rotate and open/close the vent. In the future we can improve our project by adding a CO2 sensor, solar powered batteries, or a way to communicate with the owner that would give him/her updates on if batteries need replacing or if the temperature has drastically changed. 
  
# Budget and Bill Of Materials

| Product                       	| Price  	|
|-------------------------------	|--------	|
| Vent from Resource            	| $9.21  	|
| Box from Resource             	| $2.00  	|
| LCD from Sparkfun             	| $30.32 	|
| Male to Female Adapters       	| $3.99  	|
| Servo Motor from Sparkfun     	| $31.99 	|
| Temperature & Humidity Sensor 	| $8.00  	|
| Knob                          	| $2.95  	|
| Arduino Pro Mini              	| $9.95  	|
| Solder-able Breadboard        	| $4.95  	|
| 4x 9V Batteries               	| $15.49  |

Total: $138.36  
 
Remaining  $236.64
 
  
# Timeline

  *this can also be adapted from what we already have*
  
# Appendix

## Code:
  
    #include <LiquidCrystal.h>
    #include <Servo.h> 
    #include <Wire.h> 
    Servo myservo;
    byte fetch_humidity_temperature(unsigned int *p_Humidity, unsigned int *p_Temperature);
    
    #define TRUE 1
    #define FALSE 0
    
    //int tempPin = 0;
    int lightPin = 1;
    int encoderPin1 = 2;
    int encoderPin2 = 3;
    int angle = 0; 
    
    volatile int lastEncoded = 0;
    volatile long encoderValue = 70;
    
    long lastencoderValue = 0;
    
    int lastMSB = 0;
    int lastLSB = 0;
     
    //                BS  E  D4 D5  D6 D7
    LiquidCrystal lcd(7, 8, 9, 10, 11, 12);
     
    void setup() 
    {
      myservo.attach(6);  // attaches the servo on pin 6 to the servo object
      lcd.begin(16, 4);
      pinMode(encoderPin1, INPUT); 
      pinMode(encoderPin2, INPUT);
    
      digitalWrite(encoderPin1, HIGH); //turn pullup resistor on
      digitalWrite(encoderPin2, HIGH); //turn pullup resistor on
    
      //call updateEncoder() when any high/low changed seen
      //on interrupt 0 (pin 2), or interrupt 1 (pin 3) 
      attachInterrupt(0, updateEncoder, CHANGE); 
      attachInterrupt(1, updateEncoder, CHANGE);
      
      Wire.begin();
       pinMode(4 , OUTPUT);
       digitalWrite(4, HIGH); // this turns on the HIH3610
       delay(5000);
    }
     
    void loop()
    {
      // Display Temperature in C
      byte _status;
      unsigned int H_dat, T_dat;
      int RH, T_C, T_F;
      _status = fetch_humidity_temperature(&H_dat, &T_dat);
       RH = H_dat * 6.10e-3;
       T_C = T_dat * 1.007e-2 - 40.0;
       T_F = T_C* 9.0 / 5.0 + 32.0;
      
      //int tempReading = analogRead(tempPin);
      //float tempVolts = tempReading * 5.0 / 1024.0;
      //float tempC = (tempVolts - 0.5) * 100.0;
      //int tempF = tempC * 9.0 / 5.0 + 32.0;
      //         ----------------
      
      lcd.setCursor(0, 0);
      lcd.print("Temp    F  ");
      lcd.setCursor(5, 0);
      lcd.print(T_F);
      
      //lcd.setCursor(10,0);
      //lcd.print ("T_F ");
      //lcd.setCursor (14,0);
      //lcd.print (T_F);
      
      lcd.setCursor (0,3);
      lcd.print ("Humidity    %");
      lcd.setCursor (9,3);
      lcd.print (RH);
      
      // Display Light on second row
      int lightReading = analogRead(lightPin);
      lcd.setCursor(0, 2);
      //         ----------------
      lcd.print("Light           ");  
      lcd.setCursor(6, 2);
      lcd.print(lightReading);
      delay(500);
      
      //Display Display Set Temperaure in F
      int setTemp =encoderValue;
      lcd.setCursor(0, 1);
      //
      lcd.print("Set Temp    F");
      lcd.setCursor(9, 1);
      lcd.print(setTemp);
      delay(1000);
      if (T_F < setTemp)
      {
      myservo.write(90);
      }
      else 
      {
      myservo.write(5);
      }
    }
    
    byte fetch_humidity_temperature(unsigned int *p_H_dat, unsigned int *p_T_dat)
    {
      byte address, Hum_H, Hum_L, Temp_H, Temp_L, _status;
      unsigned int H_dat, T_dat;
      address = 0x27;;
      Wire.beginTransmission(address); 
      Wire.endTransmission();
      delay(100);
      
      Wire.requestFrom((int)address, (int) 4);
      Hum_H = Wire.read();
      Hum_L = Wire.read();
      Temp_H = Wire.read();
      Temp_L = Wire.read();
      Wire.endTransmission();
      
      _status = (Hum_H >> 6) & 0x03;
      Hum_H = Hum_H & 0x3f;
      H_dat = (((unsigned int)Hum_H) << 8) | Hum_L;
      T_dat = (((unsigned int)Temp_H) << 8) | Temp_L;
      T_dat = T_dat / 4;
      *p_H_dat = H_dat;
      *p_T_dat = T_dat;
      return(_status);
    }
    
    void updateEncoder(){
      int MSB = digitalRead(encoderPin1); //MSB = most significant bit
      int LSB = digitalRead(encoderPin2); //LSB = least significant bit
    
      int encoded = (MSB << 1) |LSB; //converting the 2 pin value to single number
      int sum  = (lastEncoded << 2) | encoded; //adding it to the previous encoded value
    
      if(sum == 0b1101) encoderValue --;
      if(sum == 0b1110) encoderValue ++;
    
      lastEncoded = encoded; //store this value for next time
    }
  
## Schematic:
  ![Schematic](https://cloud.githubusercontent.com/assets/8839851/5417192/e8e12df2-81f3-11e4-8f3a-b3058138c094.png)
  
## CAD Drawings:
  
  ![Full Vent](https://cloud.githubusercontent.com/assets/8839851/5390128/3a7a9d6a-80c3-11e4-87ba-c8ad0640e321.JPG)
  
![Motor Up Close](https://cloud.githubusercontent.com/assets/8839851/5390127/3a7a616a-80c3-11e4-912e-c4b849dee82b.JPG)

![Vent](https://cloud.githubusercontent.com/assets/8839851/5390129/3a7df01e-80c3-11e4-973f-6374bf34c931.JPG)
