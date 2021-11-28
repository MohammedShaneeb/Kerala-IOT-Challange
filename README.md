
# Kerala IoT Challenge

> **Foxlab Makerspace** in association with **GTech - Group of Technology Companies** in Kerala is launching our prestigious program  **“Kerala IoT Challenge 2021”**,  with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

### About Me
> Hello Folks! I'm [**Mohammed Shaneeb**]. i am studying in +2 in PKMHHS Edarikkode (Computer Science),I am very intrested to Learn IOT, Thanks Foxlab for giving wonderfull opertunuity

## IoT Challenge Experiments

### Experiment 1 - Hello World LED Blinking

#### Things you need
* Arduino Uno Board
* USB Cable
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard
* Jumper Wires (Male to Male ) X 2 Nos


![Hello World LED Blinking](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/d8a3d600368be9a94a6b9d9b407cf64be62d7d69/IMG_20211027_233237.jpg)
#### Code
```ino
int led = 11;

void setup() {
  // put your setup code here, to run once:
  pinMode(led,OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(led,HIGH);
  delay(1000);
  digitalWrite(led,LOW);
  delay(1000);

}
```

### Experiment 2 - Traffic Light

#### Hardware required

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3
* Breadboard*1
* Breadboard jumper wires* several

![Traffic Light](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_2.jpeg)
#### Code
```ino

int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}
```

### Experiment 3 - LED Chasing Effect

#### Hardware required
* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_3.jpeg)
#### Code
```ino
int BASE = 2;
int NUM = 7;
int dly = 200;
 
 void setup() {
  // put your setup code here, to run once:
  for(int i= BASE;i<=NUM;i++){
    pinMode(i,OUTPUT);
    
  }

}

void loop() {
  // put your main code here, to run repeatedly:
  for(int i=BASE;i<=NUM;i++){
    
    digitalWrite(i,HIGH);
    delay(dly);
  }

  for(int i=NUM;i>=BASE;i--){
    digitalWrite(i,LOW);
    delay(dly);
  }

}

```

### Experiment 4 - Button Controlled LED

#### Components Required
* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_4.jpeg)
#### Code
```ino
int led = 7;
int btn = 4;

void setup() {
  // put your setup code here, to run once:
  pinMode(led,OUTPUT);
  pinMode(btn,INPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
  int val = digitalRead(btn);
  if (val == HIGH){
    digitalWrite(led,HIGH);
  }else{
    digitalWrite(led,LOW);
  }

}
```

### Experiment 5 - Buzzer

#### Components Required
* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_5.jpeg)
#### Code
```ino

void setup()
{
  pinMode(2, OUTPUT);
}

void loop()
{
  digitalWrite(2, HIGH);
  delay(500); // Wait for 500 millisecond(s)
  digitalWrite(2, LOW);
  delay(500); // Wait for 500 millisecond(s)
}
```

### Experiment 6 - RGB LED

#### Components Required
* Arduino Uno
* LED(RED,GREEN,BLUE)
* Breadboard*1
* Resistor *3
* Breadboard Jumper Wire*5
* USB cable*1

#### NOTE
   I Used Seperate RED, GREEN, BLUE LED'S . because i din'nt get RGB LED

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP6.jpeg)
#### Code
```ino

int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
```
### Experiment 7 - LDR 

#### Components Required
* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1



![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_7.jpeg)
#### Code
```ino
int led = 4;
int ldr = 0;
int ldr_value;
void setup() {
  // put your setup code here, to run once:
  pinMode(led,OUTPUT);
  pinMode(ldr,INPUT);
  Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:
  ldr_value = analogRead(ldr);
  Serial.println(ldr_value);

  if(ldr_value < 150){
    digitalWrite(led,HIGH);
    
  }else{
    digitalWrite(led,LOW);
  }

}

}
```

### Experiment 8 - Flame Sensor 

#### Components Required
* Arduino Uno Board
* IR Reciever
* LED*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*4
* USB cable*1

#### Fun Fact 
* when i fired to my sensor my jumber wires are fired and it is damaged

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_8.jpeg)
#### Code
```ino

int flame=0;// select analog pin 0 for the sensor
int LED=9;// select digital pin 9 for the LED
int val=0;
 void setup() 
{
 pinMode(LED,OUTPUT); 
 pinMode(flame,INPUT); 
 Serial.begin(9600);
void loop() 
{ 
  val=analogRead(flame);// read the analog value of the sensor 
  Serial.println(val);// output and display the analog value
  if(val>=600)// when the analog value is larger than 600, the led will glow
  {  
   digitalWrite(LED,HIGH); 
   }else 
   {  
     digitalWrite(LED,LOW); 
    }
   delay(500); 
}
```
### Experiment 9 -  LM35 Temperature sensor 

#### Components Required
* Arduino Uno Board
* LM35 Sensor
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1


![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_9.jpg)
#### Code
```ino

int sensorPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(sensorPin);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}

```


### Experiment 11 - Potentiometer analog Value Reading 

#### Components Required
* Arduino Uno Board
* Potentiometer*1
* LED*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

### ADDED
** i added a LED on output of potentiometer, so i can adjut LED's brightness

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_exp_11.jpeg)
#### Code
```ino

int vr = 0;
int val;
void setup() {
  // put your setup code here, to run once:
  pinMode(vr,INPUT);
  Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:
  val = analogRead(vr);
  Serial.println(val);

}
```
### Experiment 12 - 7 Segment Display 

#### Components Required
* Arduino Uno Board
* 1-digit LED Segment Display*1
* LED*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wire*10
* USB cable*1



![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_12.jpeg)
#### Code
```ino
int a=10;// set digital pin 7 for segment a
int b=11;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=6;// set digital pin 10 for segment d
int e=7;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp

void digital_0(void) // display number 0
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(f,HIGH);
digitalWrite(e,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(a,LOW);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,LOW);
digitalWrite(e,LOW);
digitalWrite(f,LOW);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
digitalWrite(c,LOW);
digitalWrite(d,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(e,HIGH);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,LOW);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
digitalWrite(a,HIGH);
digitalWrite(e,LOW);
digitalWrite(d,LOW);

}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}}

```
### Assignment 1 - Automatic Night Lamp 

#### Components Required
* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

LDR

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_EXP_7.jpeg)
#### Code
```ino
int led = 4;
int ldr = 0;
int ldr_value;
void setup() {
  // put your setup code here, to run once:
  pinMode(led,OUTPUT);
  pinMode(ldr,INPUT);
  Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:
  ldr_value = analogRead(ldr);
  Serial.println(ldr_value);

  if(ldr_value < 150){
    digitalWrite(led,HIGH);
    
  }else{
    digitalWrite(led,LOW);
  }

}

}
```


### Assignment 2

#### Components Required
* Arduino Uno Board
* 7 Segment Display
* LED*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wire*12
* USB cable*1

![image](https://raw.githubusercontent.com/MohammedShaneeb/Kerala-Iot-Challange/main/L1_AS_2.jpeg)
#### Video <iframe width="560" height="315" src="https://www.youtube.com/embed/6W5AEqyr68A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
#### Code
```ino
int a=10;// set digital pin 7 for segment a
int b=11;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=6;// set digital pin 10 for segment d
int e=7;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp

int btnPin = 3;
int btnState;
long ran;

void digital_0(void) // display number 0
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(f,HIGH);
digitalWrite(e,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(a,LOW);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,LOW);
digitalWrite(e,LOW);
digitalWrite(f,LOW);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
digitalWrite(c,LOW);
digitalWrite(d,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(e,HIGH);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=6;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}

void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
pinMode(3,INPUT);
randomSeed(analogRead(0));
Serial.begin(9600);
}
void loop()
{
  btnState = digitalRead(btnPin);
  if (btnState == HIGH){
    ran = random(1,7);
    Serial.println(ran);
    if (ran == 1){
      digital_1();
      delay(2000);
    }
    if (ran == 2){
      digital_2();
      delay(2000);
    }
    if (ran == 3){
      digital_3();
      delay(2000);
    }
    if (ran == 4){
      digital_4();
      delay(2000);
    }
    if (ran == 5){
      digital_5();
      delay(2000);
    }
    if (ran == 6){
      digital_6();
      delay(2000);
    }
  }
  else{
    digitalWrite(a,LOW);
    digitalWrite(b,LOW);
    digitalWrite(c,LOW);
    digitalWrite(d,LOW);
    digitalWrite(e,LOW);
    digitalWrite(f,LOW);
    digitalWrite(g,LOW);
    digitalWrite(dp,LOW);
    }
}

```
