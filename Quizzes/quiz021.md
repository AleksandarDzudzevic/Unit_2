```.py
def table()->str:
    '''

    :return: Table of 8 binary options for 3 variable bools
    '''
    ret=" | A | B | C | AB + not B + not CB \n "
    a=False
    b=False
    c=False
    x=False
    for i in range(8):
        if ((a and b) or not(b) or (not(b) and c)):
            x=True
        else:
            x=False
        ret+=(f"| {int(a)} | {int(b)} | {int(c)} | {int(x)}| \n ")
        c=not(c)
        if i and i%2==0:
            b=not(b)
        if i and i%4==0:
            a=not(a)
    return ret.center(20)
print(table())

```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/Quiz021test.png)
