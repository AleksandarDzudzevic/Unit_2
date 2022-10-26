### Mathematical solution
```.py
def numberMathces(l:int,s:int)->int:
    import math
    '''
    
    :param l: 
    :param s: 
    :return: the number of the matches needed in order to safely pass through the forest
    '''
    return math.ceil(100 * l / s / 5)
print(numberMathces(l=100,s=100))
print(numberMathces(l=500,s=150))
print(numberMathces(l=12345,s=123))
```
### While loop solution

![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz018test.png)
