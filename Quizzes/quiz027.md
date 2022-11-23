![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz027text.png)
```.py   
sensorA=[16,24,24,9,23,26,26,23,25,14]
sensorB=[2,19,25,10,11,24,17,7,24,17]
sensorC=[15,11,24,21,6,2,18,27,1,16]
import numpy as np
from matplotlib import pyplot as plt
plt.style.use('ggplot')
#step 1 create the graph of the data
# GET COLORS FROM coolors.co
# find plots on pyplot styles
time_samples=[]
for i in range(len(sensorA)):
    time_samples.append(i)
fig=plt.figure(figsize=(8,4))
plt.subplot(1,2,1)#row,col,position
plt.plot(time_samples, sensorA, color="#00e060")
plt.plot(time_samples, sensorB, color="#023047")
plt.plot(time_samples, sensorC, color="#e63946")
plt.ylabel("Sensor readings ")
plt.xlabel("Samples")
#step 2 Analyze: calculate mean and standard deviation
mean=[]
stad=[]
for s in range(len(sensorA)):
    data = [sensorA[s],sensorB[s], sensorC[s]]
    mean.append(np.mean(data))
    stad.append((np.std(data)))
plt.subplot(1,2,2)#row,col,position
plt.plot(time_samples, mean, color="#122334")
plt.fill_between(time_samples, sensorC, sensorB, alpha=.5, color="#009085")
plt.errorbar(time_samples, mean, stad, fmt='o', color='#900726')
plt.show()
```
