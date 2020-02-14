# BSA EDF Pinewood Derby Car
![Alt text](media/car.png?raw=true "Car")

My sons and I made an "outlaw" pinewood derby car for fun and to compete at the highest level at the 2020 BSA Goose Creek District Pinewood Derby.  The outlaw class is a new class for Goose Creek District Pinewood Derby.  I'll include a copy of the rules here for posterity.  The goal is to have fun, be safe, and spark an interest in engineering for the scouts.

I wanted the car to turn on and off by itself for safety and so that I didn't have to be at the starting line to press a button or deal with mechanical switches that might break.  The EDF makes more than enough thrust for vertical takeoff and I'm hoping that the perfect reaction timing will make it faster than any CO2 car at the races.  The control logic is only around 90 lines of code and contains a bug that I didn't fix, see if you can spot it.  Hint, the tinker will arm if the beam sensors are not aimed at each other when powered on during bench testing.  Note, we are absolutely abusing the battery pack and I would not recommend this setup for an airplane.  We only need 1.5 seconds of thrust for this application so we can make a tradeoff on the lightweight 4S battery.  I also removed the heat sink from the ESC to save weight.  Maybe next year will be 6S ¯\_(ツ)_/¯

## Video
[![EDF POWERED PINEWOOD DERBY CAR](https://img.youtube.com/vi/T1Uv3ryk6NY/0.jpg)](https://www.youtube.com/watch?v=T1Uv3ryk6NY)

## Controls Overview
When the IR beam is broken by the track's starting pin, the motor initially spins at a programmable lower speed.

If the beam remains broken for more than 2000 milliseconds the car is "armed" for racing.

If the car is "armed" and the starting pin drops, the IR beam is once again continuous, and the motor accelerates to full power for a specified time.  After this time, the car cannot be re-armed until the power has been removed and reapplied or the reset button on the Arduino has been pressed for safety.

## Parts List
| Description                             | Price  |
| --------------------------------------- | ------:|
| Powerfun 4300KV Ducted Fan with 40A ESC | $49 |
| Tattu 650mAh 4s 75C LIPO                | $16 |
| XT60 Connector                          | $1 |
| Adafruit Trinket 5V                     | $7 |
| IR 3mm Beam Sensor                      | $2 |
| Shipping (Amazon Prime)                 | $0 |
| Shipping (Adafruit)                     | $5 |
| **Total**                               | **$80** |

## Library Dependencies
Adafruit SoftServo - https://github.com/adafruit/Adafruit_SoftServo

Adafruit has a lot of great tutorials on getting up and running with a Trinket Arduino and their SoftServo library. It is a great little device and programming is done via a USB micro cable.  I had to use an older computer with a native USB 2.0 port.  For me, the Trinket did not work correctly with a USB 3 port.  There is a newer version of the Trinket called the Trinket M0.  I didn't have time to port the code but the Trinket M0 looks like it would be a good choice for next year's Outlaw car.

## Schematic
![Schematic](media/sketch_schem.png?raw=true "Schematic")

## Additional Pictures
![Car1](media/car1.jpg?raw=true "Car1")
![Car2](media/car2.jpeg?raw=true "Car2")
![Car3](media/car3.jpeg?raw=true "Car3")
![Car4](media/car4.jpeg?raw=true "Car4")
![Car5](media/car5.jpeg?raw=true "Car5")
