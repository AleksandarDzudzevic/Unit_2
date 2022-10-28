```.py
def get_letter(msg:str)->str:
    dict={
        'a':"4",
        'e':'3',
        'i':'1',
        'o':'0',
        ' ':'_'
    }
    case=''
    for char in msg:
        if char in dict:
            case+= dict[char]
        else:
            case+=char
    return case
print(get_letter(msg="Hello World"))
print(get_letter(msg="Why did I choose CS"))
print(get_letter(msg="Remember the Figure Caption"))
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz019test.png)
