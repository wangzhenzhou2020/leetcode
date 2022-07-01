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

```
list += []*n   # 没作用
list += [None]*n  # 才行
```
------------------------------------

String      // substring(left,right) 左闭右开 ，toCharArray()
StringBuilder  //可以用 substring、reverse()

344. 反转字符串   

541. **反转字符串 II**  // 

剑指 Offer 05. 替换空格  // 可以用 string.replace , 或者用StringBuilder() ,  或者用char[]  

151.**翻转字符串里的单词**   // 如果要修改长度，char[] 是没办法自己改变长度的，除非new char[] 。 StringBuilder比较方便修改长度.

题目：**剑指Offer58-II.左旋转字符串**  // 两次翻转即可，这里用char[] 就可以.   当然也可以用StringBuilder,  reverse() 用setCharAt()

28. **实现 strStr()**  // 更多笔记见oneNote ,  求next记住两点： next[0]=-1,  while(i<next.length-1) , 和原理。
![image](https://user-images.githubusercontent.com/67401289/176865737-0d5aa231-ca12-4b22-97b8-4932cf799bc5.png)


459. **重复的子字符串**  // 利用next[]  找规律..






