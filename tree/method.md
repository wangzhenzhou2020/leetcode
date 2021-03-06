迭代法中，一般一起操作两个树都是使用队列模拟类似层序遍历.

关于递归的参数, 有时候可以用返回值来记录变化的量，也可以用全局变量来记录变化的量。但最好能用全局变量来记录。递归的参数尽量是必要的，和当前的递归非常相关的参数，这样更简单。


递归的空间复杂度 = *每次递归的空间复杂度 * 递归深度*

中序和后序一般是O(logn)，为了保护根节点的现场。

而先序递归也是O(logn)，因为要保护根节点右孩子的现场。

二叉树的最后一层的节点数是O(n)的。即 2^( 深度 =  log2(n) ) = O(n)

**总结***

涉及到二叉树的*构造*，无论普通二叉树还是二叉搜索树一定前序，都是先构造中节点。

求普通二叉树的*属性*，一般是后序，一般要通过递归函数的返回值做计算。也有可能前序（比如求路径）。

求二叉搜索树的*属性*，一定是中序了，要不白瞎了有序性了。

-------------------------------------------------------
## JAVA

二叉树的统一迭代法   // 遇到null 就访问下一个 pop()

### 层序遍历(10道)

102. 二叉树的层序遍历  // 每一层都有一个收集。

107. 二叉树的层序遍历 II // Collections.reverse()

199. **二叉树的右视图**   // 

637. 二叉树的层平均值

429. N 叉树的层序遍历

515. 在每个树行中找最大值  //

116. **填充每个节点的下一个右侧节点指针**  // temp 节点记录上一个节点。

117. 填充每个节点的下一个右侧节点指针 II  // temp 节点记录上一个节点。

111. 二叉树的最小深度  // 

------------------------------------


226. 翻转二叉树  //

101. 对称二叉树  // 要比较的是两棵树，而不是两个节点

572. **另一棵树的子树**  // 双层递归

104. 二叉树的最大深度  //  层序最直接。也可以用前序遍历（遍历到了就求深度）。后序遍历（等子树返回高度）。

559. **N 叉树的最大深度**  //  同上

111. 二叉树的最小深度  // 这里选择用递归来做

222. **完全二叉树的节点个数**  // 有技巧。复杂度：i = 0-> logn Σ logn - i : 从1层到logn层，每层的计算量是 O(logn - i) （即while的深度）所以复杂度是 O(logn * logn)

404. 左叶子之和   // 递归和层序都可以。

513. 找树左下角的值  //  虽然递归也可以做，但层序容易理解。


236. **二叉树的最近公共祖先**  // 稍微复杂的递归逻辑，不太好想。

235. 二叉搜索树的最近公共祖先 // 可以用上题思路。但可以用二叉搜索树特性搜索。



-------------------------------------------------


110. **平衡二叉树**   //  上层满足平衡，下层不一定平衡。先从下层开始判断，如果平衡，就返回高度，帮助上层判断，否则返回-1，上层直接返回-1.


### 回溯

257. **二叉树的所有路径**   // 

112. **路径总和**  //  基本数据类型int 不是引用，可以**隐式回溯**。

113. **路径总和 II** //  257题目 + 112题目 。 int sum 隐式回溯， 路径显式回溯。




###  构造

106. **从中序与后序遍历序列构造二叉树**  // 返回节点，实现构造。 没啥技巧，细心就行。

105. **从前序与中序遍历序列构造二叉树**

654. **最大二叉树**

617. 合并二叉树  


###  二叉搜索树-遍历

700. 二叉搜索树中的搜索     // 递归 迭代 都可以

98. **验证二叉搜索树**  // 简单的思路：收集元素，判断是否递增;  复杂的思路：边递归边比较。*记录上一个节点*，而非前一个值（不方便比较）。

530. 二叉搜索树的最小绝对差  // 同样*记录上一个节点*。

501. 二叉搜索树中的众数  // *记录上一个节点*,  

538. 把二叉搜索树转换为累加树  // *记录上一个节点*

### 二叉搜索树-构造

701. 二叉搜索树中的插入操作  // 迭代就记录父节点，找到合适的空节点位置再插入。也可以用**递归构造**的方法递归插入。

450. **删除二叉搜索树中的节点**  // 迭代同样**记录父节点**, 这里用迭代的方法做的。也可以用**递归构造**的方法删除。 方法是类似的。

669. 修剪二叉搜索树  // 这里用**递归构造**的方法来修剪。root.left = traverse(), root.right = traverse() ,return root;

108. 将有序数组转换为二叉搜索树  // **递归构造** 














