---
layout: page
title: Arduino
description: >-
    Sample source codes for the Grove Arduino Beginner Kit for CWP 2.0
---

# Grove Arduino Code Samples
{:.no_toc}

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Info

This website serves as a collection of code samples for the Grove Arduino Beginner Kit. Use these code examples as a starting point and modify the code samples for your projects. 

Every project will have a set of sensors, actuators, and one microcontroller. 

Let's first look at our base board. This is what your hardware should look like: 

![Grove Arduino Board](./assets/images/grove.png)


## Components 

- Microcontroller - Arduino Uno


### Sensors 
- Button 
- Potentiometer
- Microphone (or sound sensor)
- Light Sensor
- Temperature and humidity 

### Actuators 
- LED Light 
- Servo motors 
- Speaker (or Buzzer)
- OLED Display

## Programming the Board

This is a plug and play board! Which means no wiring required unless we cut out the components. 

Let's try out some simple code examples. 

### Blinking with an LED

You need: 
- Control: Seeeduino
- Output: LED module

![LED](./assets/images/LED.png)


```
//LED Blink
//The LED will turn on for one second and then turn off for one second
int ledPin = 4;
void setup() {
    pinMode(ledPin, OUTPUT);
}
void loop() {
    digitalWrite(ledPin, HIGH);
    delay(1000);
    digitalWrite(ledPin, LOW);
    delay(1000);
}
```

### Pressing Button to Light Up LED 

You need: 
- Input: Button
- Control: Seeeduino
- Output: LED module

![Button](./assets/images/Button.png)

```
//Button to turn ON/OFF LED
//Constants won't change. They're used here to set pin numbers:
const int buttonPin = 6;     // the number of the pushbutton pin
const int ledPin =  4;      // the number of the LED pin

// variables will change:
int buttonState = 0;         // variable for reading the pushbutton status

void setup() {
  // initialize the LED pin as an output:
  pinMode(ledPin, OUTPUT);
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);
}

void loop() {
  // read the state of the pushbutton value:
  buttonState = digitalRead(buttonPin);

  // check if the pushbutton is pressed. If it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    digitalWrite(ledPin, HIGH);
  } else {
    // turn LED off:
    digitalWrite(ledPin, LOW);
  }
}
```

### Controlling the Frequency of the Blink with a Potentiometer

You need: 
- Input: Potentiometer
- Control: Seeeduino
- Output: LED module

![Potentiometer](./assets/images/rotary.png)

```
//Rotary controls LED
int rotaryPin = A0;    // select the input pin for the rotary
int ledPin = 4;      // select the pin for the LED
int rotaryValue = 0;  // variable to store the value coming from the rotary

void setup() {
  // declare the ledPin as an OUTPUT:
  pinMode(ledPin, OUTPUT);
  pinMode(rotaryPin, INPUT);
}

void loop() {
  // read the value from the sensor:
  rotaryValue = analogRead(rotaryPin);
  // turn the ledPin on
  digitalWrite(ledPin, HIGH);
  // stop the program for <sensorValue> milliseconds:
  delay(rotaryValue);
  // turn the ledPin off:
  digitalWrite(ledPin, LOW);
  // stop the program for for <sensorValue> milliseconds:
  delay(rotaryValue);
}
```

### Making the Buzzer go BEEP

You need: 
- Control: Seeeduino
- Output: Buzzer

![Buzzer](./assets/images/Buzzer.png)

```
int BuzzerPin = 5;

void setup() {
  pinMode(BuzzerPin, OUTPUT);
}

void loop() {
  analogWrite(BuzzerPin, 128);
  delay(1000);
  analogWrite(BuzzerPin, 0);
  delay(0);
}
```

*Challenge: Can you make the buzzer go beep when the button is pressed?*


### Making the Buzzer be more pleasant! 

You need: 
- Control: Seeeduino
- Output: Buzzer

Your current code is just outputting a constant PWM signal, which creates a simple (albeit annoying) buzz. To play a tune, it's better to use Arduino's tone() function, which generates specific musical notes.

![Buzzer](./assets/images/Buzzer.png)

```
int BuzzerPin = 5;

void setup() {
}

void loop() {
  // Melody notes (Hz)
  int melody[] = {
    262, 330, 392, 523,   // C4 E4 G4 C5
    392, 523, 659,        // G4 C5 E5
    784, 659, 523, 392,   // G5 E5 C5 G4
    523
  };

  // Note durations (ms)
  int duration[] = {
    150, 150, 150, 300,
    150, 150, 300,
    200, 200, 200, 200,
    500
  };

  int notes = sizeof(melody) / sizeof(melody[0]);

  for (int i = 0; i < notes; i++) {
    tone(BuzzerPin, melody[i], duration[i]);
    delay(duration[i] * 1.3);
  }

  noTone(BuzzerPin);

  delay(2000);  // Pause before repeating
}
```

*Challenge: Try out some different notes, and see what happens.*

### Sound Sensitive LED Light


You need: 
- Control: Seeeduino
- Input: Sound Sensor
- Output: LED Module


![Sound](./assets/images/Sound.png)

```
//Sound Control Light
int soundPin = A2; // Analog sound sensor is to be attached to analog
int ledPin = 4; // Digital LED is to be attached to digital
void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(soundPin, INPUT);
  Serial.begin(9600);
}
void loop(){
  int soundState = analogRead(soundPin); // Read sound sensor’s value
  Serial.println(soundState);
  // if the sound sensor’s value is greater than 400, the light will be on.
  //Otherwise, the light will be turned off
  if (soundState > 400) {
    digitalWrite(ledPin, HIGH);
    delay(100);
  }else{
    digitalWrite(ledPin, LOW);
  }
}
```

*Challenge: Now can you use the light sensor to adjust the LED?*

### Sreen time!!

For the OLED screen, we will be using an Arduino Library. 

#### Install the U8g2 library: 
Navigate to Sketch -> Include Library -> Manage Libraries... and Search for the keyword "U8g2" in the Library Manager. It's the u8g2 library by oliver, and click then install.

![U8g2-lib](./assets/images/U8g2-lib.png)

You need: 
- Seeeduino Lotus
- OLED screen 

![OLED](./assets/images/OLED.png)

```
#include <Arduino.h>
#include <U8x8lib.h>

 U8X8_SSD1306_128X64_NONAME_HW_I2C u8x8(/* reset=*/ U8X8_PIN_NONE);

// U8X8_SSD1306_128X64_NONAME_SW_I2C u8x8(/* clock=*/ SCL, /* data=*/ SDA, /* reset=*/ U8X8_PIN_NONE);   // OLEDs without Reset of the Display

void setup(void) {
  //u8x8.setBusClock(100000);  // If you breakout other modules, please enable this line
  u8x8.begin();
  u8x8.setFlipMode(1);
}

void loop(void) {
  u8x8.setFont(u8x8_font_chroma48medium8_r);
  u8x8.setCursor(0, 0);
  u8x8.print("Hello World!");
}
```

What if we want to control the screen using the Potentiometer? 

### OLED Control using Potentiometer

Let's try a fun project, where the OLED display disentegrates when you rotate the potentiometer. 

Project Plan: 
- Pot at minimum → clean "HELLO WORLD!"
- Rotate slowly → letters begin glitching into symbols.
- Rotate further → more letters corrupt.
- Near maximum → random debris appears across the screen, creating a digital disintegration look.


```
#include <Arduino.h>
#include <U8g2lib.h>
#include <Wire.h>

int rotaryPin = A0;

// Full framebuffer mode
U8G2_SSD1306_128X64_NONAME_F_HW_I2C u8g2(U8G2_R2, U8X8_PIN_NONE);

// Fast deterministic pseudo-random function
uint8_t noise8(uint16_t x, uint16_t y)
{
  uint32_t n = x * 1973UL + y * 9277UL + 89173UL;
  n = (n << 13) ^ n;
  return (n * (n * n * 15731UL + 789221UL) + 1376312589UL) >> 24;
}

void setup()
{
  u8g2.begin();
}

void loop()
{
  int pot = analogRead(rotaryPin);

  // 0 = intact, 255 = completely dissolved
  uint8_t dissolveAmount = map(pot, 0, 1023, 0, 255);

  // Draw text to framebuffer
  u8g2.clearBuffer();

  u8g2.setFont(u8g2_font_logisoso24_tf);

  const char *text = "HELLO";
  int x = 5;
  int y = 40;

  u8g2.drawStr(x, y, text);

  // Apply dissolve effect directly to framebuffer
  uint8_t *buf = u8g2.getBufferPtr();

  for (int py = 0; py < 64; py++)
  {
    for (int px = 0; px < 128; px++)
    {
      uint8_t rnd = noise8(px, py);

      if (rnd < dissolveAmount)
      {
        u8g2.setDrawColor(0);
        u8g2.drawPixel(px, py);
      }
    }
  }

  // Optional: add "dust" particles drifting away
  if (dissolveAmount > 100)
  {
    int particles = map(dissolveAmount, 100, 255, 0, 80);

    u8g2.setDrawColor(1);

    for (int i = 0; i < particles; i++)
    {
      int px = random(128);
      int py = random(64);

      if (noise8(px, py) < dissolveAmount)
      {
        // Drift right as dissolution increases
        int drift = map(dissolveAmount, 100, 255, 0, 25);

        u8g2.drawPixel(
          min(127, px + random(drift + 1)),
          py + random(-2, 3)
        );
      }
    }
  }

  u8g2.sendBuffer();

  delay(20);
}
```






