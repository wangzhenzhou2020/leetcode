[28. 实现 strStr()](https://leetcode-cn.com/problems/implement-strstr/)

```
# class Solution:
#     def strStr(self, haystack: str, needle: str) -> int:
#         # 暴力会超时：
#         if needle=='': return 0
#         len_needle = len(needle)
#         len_haystack = len(haystack)
#         for idx_h,char in enumerate(haystack):
#             idx_n = 0
#             idx_h_in = idx_h
#             while(   idx_n<len_needle 
#                   and idx_h_in < len_haystack
#                   and haystack[idx_h_in]==needle[idx_n]):
#                 idx_n += 1
#                 idx_h_in += 1
            
#             if idx_n == len_needle:
#                 return idx_h_in-len_needle
#             if idx_h_in == len_haystack:
#                 return -1     
#         return -1
       
```

KMP : 笔记见one note
```
class Solution:

    def getNext(self,s:str):        
            next = [None]*len(s)
            next[0]=-1
            i = 0
            j = -1
            while(i<len(s)-1):
                if(j==-1 or s[i]==s[j]):
                    i += 1
                    j += 1
                    next[i] = j # 最后填写next[len(s)-1]
                else:
                    j = next[j]
            return next

    def strStr(self, haystack: str, needle: str) ->int:     
        # KMP
        # 1 next 数组，定义：冲突就看门派(kmp)继续比较
        if needle=='': return 0

        next = self.getNext(needle)

        i,j = 0,0
        while(j<len(needle) and i<len(haystack)):
            if haystack[i]==needle[j]:
                i+=1
                j+=1
            else:
                j = next[j]
                if j == -1:
                    j = 0
                    i += 1
        
        # i<len(haystack) 也有可能是最后 成功了。
        if j == len(needle):
            return i-j
        else:
            return -1
```
