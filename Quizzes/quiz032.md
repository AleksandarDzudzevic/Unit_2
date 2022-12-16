![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz032text.png)
```.py
import numpy as np
import matplotlib.pyplot as plt
import requests
req = requests.get("http://192.168.6.142/readings")
data = req.json()
readings = data["readings"][0]
T=[]
T2=[]
x=[]
i=0
for r in readings:
    if r["sensor_id"]==9:
        T.append(r['value'])
        i+=1
        x.append(i)
    if r["sensor_id"]==10:
        T2.append(r['value'])
samples_per_window=12
x_per_window=[]
mean_per_window=[]
mean_per_window2=[]

count=1
for i in range(0,len(T)-12,samples_per_window):
    data=T[i:i+samples_per_window]
    data2=T2[i:i+samples_per_window]
    mean_per_window.append(sum(data)//samples_per_window)
    mean_per_window2.append(sum(data2)//samples_per_window)
    x_per_window.append(count)
    count += 1
diff=[]
for i in range(len(mean_per_window)):
    d = mean_per_window2[i]-mean_per_window[i]
    diff.append(d)
plt.subplot(3,1,1)
plt.plot(x_per_window,mean_per_window,color="blue")
plt.subplot(3,1,2)
plt.plot(x_per_window,mean_per_window2,color="red")
plt.subplot(3,1,3)
plt.plot(x_per_window,diff,color="green")
plt.show()
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz032test.png)

## B) What re three main opeartors used in boolean logic
Those are:
#### AND 
#### OR
#### NOT
