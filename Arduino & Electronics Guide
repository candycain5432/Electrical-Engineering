# Arduino & Electronics Guide

---

## 1. Introduction

**What Arduino is:**  
Arduino is an open-source electronics platform that combines **hardware** (microcontrollers) and **software** (Arduino IDE) to create interactive projects. It is beginner-friendly but also powerful enough for complex projects.  

**Popular Arduino Boards:**  
- Arduino Uno (most common)  
- Arduino Nano (compact)  
- Arduino Mega (more pins)  

**Programming Arduino with IDE:**  
1. Download and install the [Arduino IDE](https://www.arduino.cc/en/software).  
2. Connect your board via USB.  
3. Select board type and port:  
   - `Tools → Board → Arduino Uno`  
   - `Tools → Port → COMx`  
4. Write a **sketch** (Arduino program) with:  
```cpp
void setup() {
  // Initialize pins and settings
}
void loop() {
  // Main code runs repeatedly
}
```
5. Upload code using the **Upload** button.  

**Components Overview:**  
- **Outputs:** LEDs, motors, buzzers, servos  
- **Inputs:** Buttons, potentiometers, sensors  
- **Control:** Relays, ICs, transistors  
- **Prototyping:** Breadboards, jumper wires, power supply  

---

## 2. Basic Components

### 2.1 LEDs

**Description:** Light Emitting Diodes; current flows in one direction.  

**Wiring Example:**
```
Arduino Pin 13 ----[220Ω]----> LED (+)
LED (-) --------------------> GND
```

**Arduino Code Example:**
```cpp
pinMode(13, OUTPUT);
digitalWrite(13, HIGH); // LED ON
delay(500);
digitalWrite(13, LOW);  // LED OFF
delay(500);
```

---

### 2.2 Resistors

**Purpose:** Limit current in a circuit.  

**Color Code:**  
```
Black=0, Brown=1, Red=2, Orange=3, Yellow=4,
Green=5, Blue=6, Violet=7, Grey=8, White=9
```
- Example: Red-Red-Brown-Gold = 220Ω ±5%  

**Ohm's Law:**  
```
V = I * R
I = V / R
R = V / I
```

---

### 2.3 Potentiometers

**Description:** Variable resistor with 3 terminals.  
- Middle “wiper” outputs adjustable voltage.  

**Multimeter Measurement:**  
- Connect to all terminals, turn knob, observe changing voltage on wiper.  

**Arduino Example:**  
```cpp
int sensorValue = analogRead(A0);
int ledBrightness = map(sensorValue, 0, 1023, 0, 255);
analogWrite(ledPin, ledBrightness);
```

**ASCII Diagram:**
```
 VCC
  |
 [Potentiometer]
  |-----> Wiper to Arduino analog pin
 GND
```

---

### 2.4 Buttons

**Description:** Simple digital input.  

**Wiring with Pull-Down Resistor:**
```
5V ----O O---- Arduino Pin
       |
      10kΩ
       |
      GND
```

**Arduino Code Example:**
```cpp
pinMode(buttonPin, INPUT);
if(digitalRead(buttonPin) == HIGH){
  // button pressed
}
```

---

## 3. Arduino Projects

### 3.1 Blinking LED
```cpp
void setup() {
  pinMode(13, OUTPUT);
}
void loop() {
  digitalWrite(13, HIGH);
  delay(500);
  digitalWrite(13, LOW);
  delay(500);
}
```

---

### 3.2 Button-Controlled LED
```cpp
bool ledState = false;

void loop() {
  if(digitalRead(buttonPin) == HIGH){
    ledState = !ledState; // toggle
    digitalWrite(ledPin, ledState ? HIGH : LOW);
    delay(200); // debounce
  }
}
```

---

### 3.3 Simon Says Game
- Use **4 LEDs** and **4 buttons**.  
- Arduino generates a sequence of lights.  
- Player repeats sequence.  
- Increment length each round.  

**Tips:** Use arrays to store sequence and check input.

---

### 3.4 Potentiometer-Controlled Servo
```cpp
#include <Servo.h>
Servo myServo;

void setup(){ 
  myServo.attach(9); 
}

void loop(){
  int potVal = analogRead(A0);
  int angle = map(potVal, 0, 1023, 0, 180); // safe limits
  myServo.write(angle);
  delay(15);
}
```

---

### 3.5 LED Dimmer using PWM
- Use `analogWrite(pin, value)` to adjust LED brightness.  
- Value range: 0 (off) to 255 (full brightness).

---

### 3.6 High-Current LEDs with Transistor
```
Arduino Pin ----> Base
Collector ----> LED (+) ----> VCC
Emitter ----> GND
```
- Protects Arduino from high current.  
- Use NPN transistor or logic-level MOSFET.  
- Optional: add diode across LED for reverse protection.

---

## 4. Servo Motors

**Function:** Rotate to specific angles using PWM signal.  
- Torque: rotational force; must match load.  

**Projects:**  
- Robotic arms  
- Flap mechanisms  
- Animatronic movement  
- Catapults or launchers  

**Tip:** Always avoid overloading servo mechanically.

---

## 5. Relays

**Function:** Electrically operated switch.  
- Isolates Arduino from high voltage circuits.  

**Wiring Example:**
```
Arduino Pin -> IN Relay Module
GND --------- GND
VCC --------- 5V
Relay COM --- Load1
Relay NO ---- Load2
```

**Safety:**  
- Never touch high-voltage terminals  
- Use transistor protection for Arduino control  

**Example Project:** Control a lamp or motor safely.

---

## 6. Multimeter Basics

**Functions:**  
- DCV: DC Voltage  
- ACV: AC Voltage  
- DCA: DC Current  
- Continuity: detect connections  
- HFE: measure transistor gain  

**Tips:**  
- Always start with highest range if unsure.  
- Test batteries, resistors, diodes, potentiometers.

---

## 7. Integrated Circuits (ICs)

**Description:** Packaged electronic circuits.  
- Types: Digital, Analog, Mixed-signal  

**Examples:**  
- 555 Timer → Blinking LEDs, tone generation  
- LM358 Op-Amp → Amplify sensors  
- 74HC00 → Logic gates  
- ATmega328 → Arduino microcontroller  

**Tips:**  
- Check datasheet for pinout and limits  
- Insert in correct orientation (notch aligns pin 1)

---

## 8. Circuit Design & Breadboarding

**Breadboard Tips:**  
- Power rails: VCC (+) / GND (-)  
- Rows for components, columns are connected  

**Example Circuits:**  
- LED + Potentiometer dimmer  
- Servo + Potentiometer  
- Relay + Arduino + Lamp  

**Tools:**  
- Tinkercad Circuits  
- Fritzing  
- KiCAD  

---

## 9. Safety Tips

- Stay within voltage/current limits  
- Avoid overloading servos mechanically  
- Disconnect AC before wiring  
- Double-check connections  
- Use protective resistors with LEDs

---

## 10. Additional Resources

**ICs:** 555, LM358, 74HC00, ATmega328  
**Libraries:** Servo, Wire, EEPROM, Adafruit PWM  
**Websites:** Arduino.cc, All About Circuits, SparkFun, Digi-Key  

---

## 11. Example ASCII Diagrams

**LED Circuit:**
```
+5V
 |
[220Ω]
 |
|>| LED
 |
GND
```

**Button with Pull-Down Resistor:**
```
5V ----O O---- Arduino Pin
       |
      10kΩ
       |
      GND
```

**Potentiometer Voltage Divider:**
```
 VCC
  |
 [Potentiometer]
  |-----> Wiper to Arduino analog pin
 GND
```

**Relay Control:**
```
Arduino Pin -> IN Relay Module
GND ----------- GND
VCC ----------- 5V
Relay COM ----- Load1
Relay NO ------ Load2
```
