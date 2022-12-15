![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quizz025text.png)
```.py
def produce(n:int,m:int,s:int):
    import random
    random.seed(1234)
    x_out=[]
    y_out=[]
    z='|        x        |       y(x)        |\n'.center(10)
    for i in range(100):
        x=-10+0.2*i
        x_out.append(x)
        y=abs(x).__round__(2)
        y_out.append(y)
        z+=(f"|   {str(x).center(10)}    |    {str((y).__round__(2)).center(10)}     |\n").center(10)
    return y_out,x_out
data_y,data_x=produce(n=100,m=3,s=2)
from matplotlib import pyplot as plt
plt.plot(data_x,data_y,color="red",marker=".")
plt.ylabel("$y=|x|$")
plt.xlabel("Variable X")
plt.show()
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz025test.png)
