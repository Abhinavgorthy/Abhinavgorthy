#include <Servo.h>
Servo myservo1;
Servo myservo2;
int pos = 0;
int trigpin=8;
int echopin=13;

void setup()
{
 pinMode(trigpin,INPUT);
 pinMode(echopin,OUTPUT);
 pinMode(12,OUTPUT);
 pinMode(7,OUTPUT);
 myservo1.attach(12);
 myservo2.attach(7);
 Serial.begin(9600);
}

void loop()
{
   digitalWrite(trigpin,HIGH);
  delay(1500);
  digitalWrite(trigpin,LOW);
  delay(1500);
  int duration=pulseIn(echopin,HIGH);
  int distance=(duration*0.032)/2;
  Serial.println("the distance is..");
  Serial.println(distance);
  if(distance>>100)
  {
    for (pos = 0; pos <= 180; pos += 1)
    { 
  myservo1.write(pos);
  myservo2.write(pos);
  delay(1000);                      
    } 
    for (pos = 180; pos >= 0; pos -= 1) 
  {     
  myservo1.write(pos);
  myservo2.write(pos);
  delay(1000);   
  }
  }
  
  else 
  {
    pos = 0;
    {
      myservo1.write(pos);
      myservo2.write(pos);
      delay(1000); 
     }
    
  }
}

