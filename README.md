# NotSoBasicArduino
 The follwing files are my second foray into Arduino
 
 
## Table of Contents
* [Table of Contents](#TableOfContents)
* [LED_Fade](#LED_Fade)
* [Finite Led](#Finite_Led)
* [FillMeInLAter](#FillMeInLAter)
---

## LED_Fade

### Description & Code

```C++
int led = 9;           
int brightness = 0;    
int fadeAmount = 5;    

void setup() {
  pinMode(led, OUTPUT);
}

void loop() {
  
  analogWrite(led, brightness);

  
  brightness = brightness + fadeAmount;

 
  if (brightness <= 0 || brightness >= 255) {
    fadeAmount = -fadeAmount;
  }
  
  delay(30);
}

```


### Evidence
https://create.arduino.cc/editor/rareval48/4b6e7dc3-a2c5-4d0c-a7ee-7332df49a15a/preview

### Images
<img src="https://user-images.githubusercontent.com/71342195/101519720-81ef2600-3951-11eb-9d2e-db70f7997b2c.png">

---
## Finite_Led

### Description & Code
```C++
int LED1 = 9; //Labels for the leds
int LED2 = 8;
int counter1 = 1;

void setup()
{
  pinMode(LED1, OUTPUT); 
  pinMode(LED2, OUTPUT);
}

void loop(){
if (counter1 < 6) // How many times the led should blink
{
  digitalWrite(LED1, HIGH);
  delay(500);
  counter1 = counter1 + 1;
  digitalWrite(LED1, LOW);
  delay(500);
}

if (counter1 < 6)
{
  digitalWrite(LED2, HIGH);
  delay(500);
  counter1 = counter1 + 1;
  digitalWrite(LED2, LOW);
  delay(500);
}
}
```
### Evidence
https://create.arduino.cc/editor/rareval48/e87eaecd-4314-4d98-b8c2-037e3244c2f8/preview

### Images
<img src="https://user-images.githubusercontent.com/71342195/100011973-8ab3f980-2da0-11eb-9dd5-2ba529c26f8a.png">

---
## Button_Controlled_LED

### Description & Code
```C++
int LED = 8;
int buttonState = 0;
int buttonPin = 7;
int delayVar = 1000;

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin 13 as an output.
  pinMode(LED, OUTPUT);
  pinMode(buttonPin, INPUT);
  Serial.begin(9600); // This turns on my Serial Monitor
}





void loop() {
  buttonState = digitalRead(buttonPin);
  Serial.print("button State: ");
  Serial.print(buttonState);

  if (buttonState == HIGH) {
    blink(delayVar);
    Serial.print("\t delayVar:");
    Serial.println(delayVar);
    if (delayVar > 100)
      delayVar = delayVar - 100;
  }
  else
  {
    digitalWrite(LED, LOW);            // turn the LED off by making the voltage LOW
    delayVar = 1000;
    Serial.println("\t no blink!");

  }
}





void blink(int x) {
  digitalWrite(LED, HIGH);           // turn the LED on (HIGH is the voltage level)
  delay(x);                       // wait for a second
  digitalWrite(LED, LOW);            // turn the LED off by making the voltage LOW
  delay(x);                       // wait for a second
}


}
```
### Evidence
https://create.arduino.cc/editor/rareval48/1b0a8913-cb79-47c5-bea5-1da8c539bca8/preview

### Images
<img src="https://user-images.githubusercontent.com/71342195/101520864-0aba9180-3953-11eb-9b87-670dba7babae.png">
