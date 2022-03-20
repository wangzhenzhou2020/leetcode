str是不能赋值修改的，**str->list->str**

```
a,b = b,a
s[i],s[j] = s[j],s[i]
```

```
str.split()  # 用空格切分 str -> [word_1,...,word_end]
list(str)    # [char1,...,char_end]
''.join(list) # list->str
```
