 数组的速度 还是 要比 hash快的。因为hash 是**平均 o(1)**，而数组是o(1)。前提是*数据范围较小*
 
 
 当要快速查询 ，一个元素的相关属性时，用 *dict*
 
 快速查询一个元素 是否存在时 ，用 *set*
 
 *dict* 字典存储的作用：遍历过后，再次访问的复杂度是o(1)，适合于一些**需要再次访问的场景**。
 
 **暴力解**往往是for 循环内部的数据重复访问了多次。而hash*dict*通过记录之前访问过的数据（比较外层的 for 循环），
 
 **使得for 循环层数 减少**，需要时直接查找 即可。
 
242. **有效的字母异位词**   //  用数组会更快

383. 赎金信  //  类似 242.

349. 两个数组的交集  // 输出结果不唯一, 这里用预排序+双指针的方法

202. **快乐数**   // 非常好的题目。读懂题意。

1. **两数之和**  // 

454. **四数相加 II**  // 巧妙。

15. **三数之和**   

//其实这道题目使用哈希法并不十分合适，因为在去重的操作中有很多细节需要注意，在面试中很难直接写出没有bug的代码。**排序 + 二分查找**
                
// 若题目要求返回 值，可以排序，若题目要求返回下标，则**不可以排序**。    
                 
```
res.add(Arrays.asList(nums[i], nums[left], nums[right]));
```               

18. **四数之和**   // 也要去重，返回值。 **排序 + 二分查找** 

```
res.add(Arrays.asList(nums[i],nums[j], nums[left], nums[right]));
```
