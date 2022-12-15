![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz029text.png)
```.py
def count_letters(lexicon:dict,msg:str)->str:
    for i in range(len(msg)):
        if msg[i] in lexicon.keys():
            lexicon[msg[i]]+=1
    return lexicon
vowels={'a':0,"e":0,"i":0,"u":0,"o":0}
case1=(count_letters(vowels,"hello world"))
print(case1)
vowels={'a':0,"e":0,"i":0,"u":0,"o":0}
case2=count_letters(vowels,"testing number two")
print(case2)
```
![](https://github.com/AleksandarDzudzevic/Unit_2/blob/main/quiz029test.png)
