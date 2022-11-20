![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz023text.png)
```.py
def produce(n:int,m:int,s:int):
    import random
    random.seed(1234)
    x_out=[]
    y_out=[]
    a=0.5*((m/s)**2)
    z='|        x        |       y(x)        |\n'.center(10)
    for i in range(n):
        x=random.randint(0,100)
        x_out.append(x)
        y=(x**a).__round__(2)
        y_out.append(y)
        z+=(f"|   {str(x).center(10)}    |    {str((x**a).__round__(2)).center(10)}     |\n").center(10)
    return y_out,x_out
data_y,data_x=produce(n=100,m=3,s=2)
from matplotlib import pyplot as plt
plt.plot(data_x,data_y,color="red",marker="*")
plt.ylabel("$y=x^{1/2(m/s)^2}$")
plt.xlabel("Variable X")
plt.show()
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz023test.png)
### Part b) Table
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz022table.jpg)
