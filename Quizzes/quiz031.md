![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz031text.png)
```.py
#example api: aplication programing interface
import matplotlib.pyplot as plt
import numpy as np
import requests
req = requests.get("http://192.168.6.142/readings")
data = req.json()
readings = data["readings"][0]
T=[]
x=[]
i=0
for r in readings:
    if r["sensor_id"]==1:
        T.append(r['value'])
        i+=1
        x.append(i)
plt.style.use('ggplot')
plt.scatter( x[610:800],T[610:800], color="#00e060")
#LINEAR
m,b=np.polyfit(x[610:800],T[610:800],1)
print(f"Linear equation is y={m:.2f}x+({b:.2f})")
y_model=[]
for i in x[610:800]:
    y_model.append(m*i+b)
plt.plot(x[610:800],y_model,color="green")
#QUADRATIC
y_quad=[]
p0,p1,p2 = np.polyfit(x[610:800],T[610:800],2)#2 means power of 2
for i in x[610:800]:
    y_quad.append(p0*(i**2)+p1*i+p2)
plt.plot(x[610:800],y_quad,color="blue")
plt.show()

```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz031test.png)
