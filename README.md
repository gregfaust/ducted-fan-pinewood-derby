# BSA EDF Pinewood Derby Car
![Alt text](media/car.png?raw=true "Car")

I made an "outlaw" pinewood derby car for fun but also was hoping to spark an interest in engineering for a few young minds as well.

She's not much to look at admittedly but speed was the primary goal. I wanted the car to turn on and off by itself so that I didn't have to be at the starting line to press a button or be at the finish to turn it off. The EDF makes enough thrust at full power to take off vertically so it is as fast as possible without getting into CO2. The build cost around $75 and the control logic is only around 90 lines of code.  I used cheapish hobby components with reserve capacity to hopefully mitigate failures.

## Video
[![EDF POWERED PINEWOOD DERBY CAR](https://img.youtube.com/vi/T1Uv3ryk6NY/0.jpg)](https://www.youtube.com/watch?v=T1Uv3ryk6NY)

## Controls Overview
When the IR beam is broken by the track's starting pin, the motor initially spins at a programmable lower speed.

If the beam remains broken for more than 2000 milliseconds the car is "armed" for racing.

If the car is "armed" and the starting pin drops, the IR beam is once again continuous, and the motor accelerates to full power for a specified time.  After this time, the car cannot be re-armed until the power has been removed and reapplied or the reset button on the Arduino has been pressed for safety.

## Parts List
| Description                            | Price  |
| -------------------------------------- | ------:|
| Poerfun 4300KV Ducted Fan with 40A ESC | $49 |
| Tattu 650mAh 4s 75C LIPO               | $16 |
| XT60 Connector                         | $1 |
| Adafruit Trinket 5V                    | $7 |
| IR 3mm Beam Sensor                     | $2 |
| Shipping (Amazon)                      | $0 |
| Shipping (Adafruit)                    | $5 |
| **Total**                              | **$80** |

## Library Dependencies
Adafruit SoftServo - https://github.com/adafruit/Adafruit_SoftServo

Adafruit has a lot of great tutorials on getting up and running with a Trinket Arduino and their SoftServo library. It is a great little device and programming is done via a USB micro cable.

## Schematic
![Schematic](media/sketch_schem.png?raw=true "Schematic")

## Additional Pictures
![Car1](media/car1.jpg?raw=true "Car1")
![Car2](media/car2.jpeg?raw=true "Car2")
![Car3](media/car3.jpeg?raw=true "Car3")
![Car4](media/car4.jpeg?raw=true "Car4")
![Car5](media/car5.jpeg?raw=true "Car5")
