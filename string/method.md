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

 python 的list 是一个怪胎，元素可以是字符串。

而C++ 的str，是不能作为一维数组的元素的，一维数组的元素只能是char

```
l_s = [...]
l_s[0:len(s)-n].reverse() # 这样是创建了新的list了
```
