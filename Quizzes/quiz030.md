![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz030text.png)
```.py
import numpy as np
from matplotlib import pyplot as plt
h = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
samples_per_window=4
mean_per_window=[]
mean_of_overlap=[]
x_per_window=[]
x_overlap=[]
y_overlap=[]
count=0
for i in range(0,len(h),samples_per_window):
    data=h[i:i+samples_per_window]
    mean_per_window.append(sum(data)//samples_per_window)
    x_per_window.append(count)
    count += 1
for i in range(0,len(h),2):
    data=h[i:i+samples_per_window]
    y_overlap.append(sum(data)//samples_per_window)
    x_overlap.append(i)

#now we need to create an error bar
plt.style.use('ggplot')
fig = plt.figure(figsize=(14,8),dpi=400)
plt.subplot(2,1,1)
plt.plot(x_per_window, mean_per_window,'o-', color="#122334")
plt.subplot(2,1,2)
plt.plot(x_overlap,y_overlap,'o-')
plt.show()


```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz030test.png)
### A} When was internet first created?
ARPANET adopted TCP/IP on January 1, 1983, and from there researchers began to assemble the “network of networks” that became the modern Internet. The online world then took on a more recognizable form in 1990, when computer scientist Tim Berners-Lee invented the World Wide Web. While it’s often confused with the internet itself, the web is actually just the most common means of accessing data online in the form of websites and hyperlinks. 
Sources:

Andrews, Evan. “Who Invented the Internet?” History.com, A&amp;E Television Networks, 18 Dec. 2013, https://www.history.com/news/who-invented-the-internet. 
