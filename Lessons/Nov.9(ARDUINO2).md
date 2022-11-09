![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/Arduino%20task%20text.png)
## BILL OF MATERIALS
1 Breadboard
1 blue USB cable
1 Arduino Uno version R3
3 LED’s 
8 wires
3 resistors 
```.py
from pyfirmata import Arduino
import time

board =Arduino('/dev/cu.usbserial-110')
print("Communication successfully started")
a=False
b=False
c=False
i=input("ENTER THE NUMBER")
while not i in[0,1,2,3,4,5,6,7]:
    print("ERROR WRONG INPUT, PLEASE ENTER AN INTIGER BETWEEN 0-7")
    i=input()
    if i.isdigit():
        i=int(i)
if i%2==1:
    c=not(c)
if i//4==1:
    a=not(a)
if i%4>1:
    b=not(b)
board.digital[12].write(int(c))
board.digital[9].write(int(b))
board.digital[5].write(int(a))
time.sleep(0.5)
```
