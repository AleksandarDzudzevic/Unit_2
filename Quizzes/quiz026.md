![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz026text.png)
```.py
import numpy as np
x_model=[]
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
for i in range(len(h)):
    x_model.append(i)
from matplotlib import pyplot as plt
plt.scatter(x_model,h,color="red")
plt.ylabel("Variable Y number of stinkbugs in TAC 2")
plt.xlabel("Variable X temperature in degrees")
m,b=np.polyfit(x_model,h,1)
print(f"Linear equation is y={m:.2f}x+({b:.2f})")
y_model=[]
plt.ylabel("Relative humidity %")
plt.xlabel("Samples")
for i in x_model:
    y_model.append(m*i+b)
plt.plot(x_model,y_model,color="green")
plt.show()
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz026test.png)
