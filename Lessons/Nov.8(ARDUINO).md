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

board =Arduino('/dev/cu.usbserial-10')
print("Communication successfully started")
a=False
b=False
c=False
for i in range(1,9):
   c=not(c)
   if i and i%2==0:
       b=not(b)
   if i and i%4==0:
       a=not(a)
   board.digital[12].write(int(c))
   board.digital[9].write(int(b))
   board.digital[5].write(int(a))
   time.sleep(1)
```
## VIDEO LINK:
https://drive.google.com/file/d/1bObtO1tIcPXlbysXwr-98ypaShrhBinA/view?usp=sharing
