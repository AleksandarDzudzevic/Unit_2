![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz020text.png)
```.py
def table()->str:
    '''

    :return: Table of 8 binary options for 3 variable bools
    '''
    ret=" | A | B | C | \n _____________ \n "
    a=False
    b=False
    c=False
    for i in range(1,9):
        ret+=(f"| {int(a)} | {int(b)} | {int(c)} | \n ")
        c=not(c)
        if i and i%2==0:
            b=not(b)
        if i and i%4==0:
            a=not(a)
    return ret.center(20)
print(table())
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz020test.png)
### Table binary and circut
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/IMG_20221103_221339.jpg)
