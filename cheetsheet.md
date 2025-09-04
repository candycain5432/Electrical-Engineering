# 🛠️ Arduino & Electronics Beginner Cheat Sheet

## 1. Introduction
- **Arduino**: Open-source platform for interactive electronics.
- **Programming**: Use Arduino IDE (C++-based sketches).
- **Core Components**: LEDs, resistors, potentiometers, buttons, servos, relays, ICs.

## 2. Basic Components
- **LEDs**: Polarized; use resistor; control with `digitalWrite`.
- **Resistors**: Limit current; use Ohm’s Law `V = I × R`.
- **Potentiometers**: Variable resistor; adjust voltage; control brightness/servo.
- **Buttons**: Digital input; use pull-up/down resistors.

## 4. Servo Motors
- **Servos**: Motors with angle feedback.
- **Torque**: Match strength to load.
- **Uses**: Robotic arms, flaps, animatronics.

## 5. Relays
- **Relay**: Switch high-voltage with low-voltage signal.
- **Control**: Arduino triggers coil; coil switches load.
- **Project Tip**: Use transistor to protect Arduino.

## 6. Multimeter Basics
- **Functions**: DCV/ACV (voltage), DCA (current), continuity, resistance, HFE.
- **Use Cases**: Measure voltage/current; test resistors, pots, diodes.

## 7. Integrated Circuits (ICs)
- **ICs**: Chips with multiple functions.
- **Types**: Digital, analog, mixed.
- **Examples**:
  - 555 Timer: Pulse gen
  - LM358: Op-amp
  - 74HC00: Logic gate
  - ATmega328: Arduino MCU

## 8. Circuit Design & Breadboarding
- **Breadboard Tips**: Avoid high current; keep wiring clean.
- **Example Circuits**: LED dimmer, servo control, relay lamp.
- **Tools**: Tinkercad, Fritzing, EasyEDA.

## 9. Safety Tips
- Respect voltage/current limits.
- Avoid servo overload.
- Handle AC/DC loads with care.

## 10. Resources
- **Components**: LEDs, resistors, pots, buttons, servos, relays.
- **Libraries**: Servo, NeoPixel, LiquidCrystal.
- **Websites**: Arduino tutorials, SparkFun, Adafruit, Tinkercad.
