![image](https://user-images.githubusercontent.com/67401289/178138227-09644523-64b4-4820-9057-2b70a2f56709.png)

455.分发饼干    

376. **摆动序列**  //  画图 ， 也可以动态规划

53. **最大子序和**  // 画图，分析，找规律，也可以动态规划

122.买卖股票的最佳时机II  //

55. **跳跃游戏**  // 

378. **跳跃游戏 II**  // 举例，画图，分析。

1005. **K 次取反后最大化的数组和**  //举例， 分析 。 先翻负数，再翻最小正数。 JAVA Arrays.Sort() 只能自定义 泛型排序，没法儿自定义 基本类型排序。

134. **加油站**  // 不好想。需要仔细分析，降低复杂度O(n2) -> O(n)。否则超时。 不知道哪里用贪心了？

135. 分发糖果  // 这个直接不会。随想录的题解不好理解。https://www.bilibili.com/video/BV1cS4y1z7so?spm_id_from=333.337.search-card.all.click&vd_source=8227479b71e61182247876d99eb8d179

406. 根据身高重建队列  // 这尼玛也太难想了.数组本身就是对象
```
LinkedList<int[]> que = new LinkedList<>();
        for(int[] p : people)
            que.add(p[1],p);
return que.toArray(new int[people.length][]);
```

452. 用最少数量的箭引爆气球  // 图画的不好，就做不出来！！！

452. 用最少数量的箭引爆气球 // int 数据类型排序，不能直接return o1-o2, 有可能**溢出**！！

714. 买卖股票的最佳时机含手续费  // 应该用动态规划解决比较方便。

968. 监控二叉树  // 搞不出来
