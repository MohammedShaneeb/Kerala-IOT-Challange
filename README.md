
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

![image](https://user-images.githubusercontent.com/44474792/132120819-7dca413d-2dbe-41b3-9929-c44915715aa0.jpg)
#### Code
```ino
void setup() 
{ 
  pinMode(8, OUTPUT);
} 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```


