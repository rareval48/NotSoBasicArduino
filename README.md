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
Description goes here

Here's how you make code look like code:

```C++
// set the brightness of pin 9:
  analogWrite(led, brightness);

  // change the brightness for next time through the loop:
  brightness = brightness + fadeAmount;

  // reverse the direction of the fading at the ends of the fade:
  if (brightness <= 0 || brightness >= 255) {
    fadeAmount = -fadeAmount;
  }
```
Talk about how the fade works, here....

### Evidence
https://create.arduino.cc/editor/helmstk1/9e044cca-43d7-4d93-885f-e6dec5b4f769/preview

### Images


---
## Finite_Led

### Description & Code

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

### Evidence
https://create.arduino.cc/editor/rareval48/e87eaecd-4314-4d98-b8c2-037e3244c2f8/preview

### Images
<img src="https://user-images.githubusercontent.com/71342195/100011973-8ab3f980-2da0-11eb-9dd5-2ba529c26f8a.png">
