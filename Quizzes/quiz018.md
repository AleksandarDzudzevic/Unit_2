![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz018text.png)
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
```.py
def numberMathces(l,s):
    lyli_position=0
    speed_m_s=s/100
    seconds_passed=0
    matches=0
    while lyli_position<l:
        seconds_passed+=1
        lyli_position+=speed_m_s
        if seconds_passed==5:
            matches+=1
            seconds_passed=0
    if lyli_position!=l:
        matches+=1
    return matches
print(numberMathces(l=100,s=100))
print(numberMathces(l=500,s=150))
print(numberMathces(l=12345,s=123))
```
### Mathematical solution test
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz018test.png)
### While loop solution test
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz018test2.png)
