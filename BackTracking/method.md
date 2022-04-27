可以抽象为一个n叉树
```
返回值 void backTracking() 
if(end_condiction):
    # 收集结果;
    return;
 
for(集合元素) 单层搜索逻辑
    #处理节点
    #backTracking()；
    #回溯；撤销处理的节点
```
for循环可以理解是横向遍历，backtracking（递归）就是纵向遍历。
回溯法是一些问题的暴力搜索方法。本质是穷举。




77. 组合   这里，每个节点，是一个序列（for循环）。
17. 电话号码的字母组合  限制了每个位置的数字
