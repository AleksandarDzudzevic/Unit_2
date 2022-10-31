
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz017text.png)
```.py
def avaragewordlength(list:str)->float:
    cnt=0
    sum=0
    for i in range(0,len(list)):
        sum+=len(list[i])
        cnt+=1
    return sum/cnt
print(avaragewordlength(list=["Hello","main"]))
print(avaragewordlength(list=["Peru","France","Nepal"]))
print(avaragewordlength(list=["Computer Science","Art"]))
print(avaragewordlength(list=["one","two"]))
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz017test.png)
## HL
```.py
def avaragewordlength(list:str)->float:
    cnt=0
    sum=0
    for i in range(0,len(list)):
        sum+=len(list[i].strip())
        cnt+=1
    return sum/cnt
print(avaragewordlength(list=["Hello ","main"]))
print(avaragewordlength(list=["Peru         ","France","Nepal"]))
print(avaragewordlength(list=["Computer Science","Art"]))
print(avaragewordlength(list=["one","two"]))
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz017test2.png)
