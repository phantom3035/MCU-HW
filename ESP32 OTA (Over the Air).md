---
layout: post
title: ESP32 GPIO
author: [Richard Kuo]
category: [Lecture]
tags: [jekyll, ai]
---

Introduction to GPIO pin functions (debounce, pullup, interrupt), OneWire interface with DS18B20, DHT11, and IR Remote.

---
## MCU - Micro Control Unit (Microcontroller)
A MCU consist of a processor core, memory and I/O interfaces

NodeMCU-32S pinout<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/NodeMCU-32S_pinout.jpg?raw=true)

---
## GPIO (General Purpose I/O)
![](https://github.com/rkuo2000/MCU-course/blob/main/images/GPIO_circuit_diagram.png?raw=true)

Each IO pad drive/sink **~25mA**, Entire Chip drive/sink **~200mA**<br>
![](https://github.com/rkuo2000/MCU-course/blob/main/images/GPIO_LED_circuit.png?raw=true)

---
### Arduino Digital IO
**GPIO write**<br>
* defines:
`#define ledPin 2`

* setup():
`pinMode(ledPin, OUTPUT);`

**GPIO read**<br>
* defines:
`#define sensorPin 23`

* setup():
`pinMode(sensorPin, INPUT);`

* loop():
`sensor_state = digitalread(sensorPin);`

---
### Examples/01.Basics/Blink
* NodeMCU-32S has a built-in LED on GPIO2.<br>
`#define LED_BUILTIN 2`

* **setup()** : *To setup MCU's default value, setup() is run only once after power-up or reset*
```
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}
```

* **loop()**: *The main is loop() that keeps running forever.*
```
// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```

---
### Sensors
**Passive InfraRed sensor: PIR** (人體紅外線感應)
![](https://solderingmind.com/wp-content/uploads/2019/06/Motion-sensor-connection.png)

**Reflective InfraRed sensor: TCRT5000** (反射式光電開關)
![](https://64.media.tumblr.com/6ca8b4893c313e82d70b8f8d0cd28e97/tumblr_inline_og893qxV8p1t7dg2q_1280.jpg)
<table>
<tr>
<td><img src="https://www.hkstem.club/wp-content/uploads/2018/06/TCRT5000.jpg"></td>
<td><img src="http://www.elecrow.com/download/TCR5000L1.jpg"></td>
</tr>
</table>


---
### Examples/Stepper/MotorKnob
![](https://github.com/rkuo2000/MCU-course/blob/main/images/Examples_Stepper_MotorKnob.png?raw=true)

<br>
<br>

*This site was last updated {{ site.time | date: "%B %d, %Y" }}.*


