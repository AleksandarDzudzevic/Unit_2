![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz022text.png)
```.py
def produce(n:int,m:int,s:int)->str:
    import random
    random.seed(1234)
    a=0.5*((m/s)**2)
    z='|        x        |       y(x)        |\n'.center(10)
    for i in range(n):
        x=random.randint(0,100)
        z+=(f"|   {str(x).center(10)}    |    {str((x**a).__round__(2)).center(10)}     |\n").center(10)
    return z
print(produce(n=5,m=3,s=2))
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz022test.png)
