
## 1. 路径之和 ii

- 来源： [leetcode 113](https://leetcode-cn.com/problems/path-sum-ii/)
- 问题：给定一个二叉树和一个目标和，找到所有从根节点到叶子节点路径总和等于给定目标和的路径。‘


### 思路

- 从根节点深度遍历二叉树， 先序遍历时，将该节点值存储在path栈中， 使用path_value 累加节点值
- 当遍历至叶节点时，检查path_value 值是否为sum， 若为sum， 则将path push到result 结果中
- 在后序遍历时，将该节点从path栈中弹出，path_value 减去节点值


**尝试使用非递归版本来做一下。**

## 2. 最近的公共祖先

- 来源： [leetcode 236](https://leetcode-cn.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- 题目：已知一个二叉树，求二叉树中给定两个节点的最近公共祖先

### 分析

1. 两个节点的公共祖先一定在从根节点，至这两个节点的路径上
2. 由于求公共祖先中的最近公共祖先，那么即同时出现在这两条路径上的离根节点最远的节点
3. 算法即： 求p节点路径，q节点路径， 两路径上最后一个相同的节点

### 思路

先求 p 节点， q节点路径，然后找到两个路径上最后一个相同的节点， 因此关键在于如何在一棵二叉树中找到一个节点的路径。

采用先序遍历的过程，只要遇到该节点，就将当前的栈赋予即可
## 3. 二叉树展开为链表

- 来源：**[leetcode 114](https://leetcode-cn.com/problems/flatten-binary-tree-to-linked-list/)**
- 题目：给定一个二叉树，将该二叉树原地转换为单链表， 单链表中的节点顺序为二叉树前序遍历顺序。

### 思路1

采用前序遍历，将node 存入到一个vector中， 然后遍历vector就行了。

### 思路2

需要重新看

## 4. 二叉树的右视图

- 来源：[leetcode 199](https://leetcode-cn.com/problems/binary-tree-right-side-view/)
- 问题： 给定一棵二叉树，想象自己站在它的右侧，按照从顶部到底部的顺序，返回从右侧所能看到的节点值。

### 思路

其本质上就是层次遍历二叉树时，记录每一层中出现的最后一个节点。

思路; 层次遍历时，将 节点和层数绑定为pair， 压入队列时，将节点与层数同时压入队列，并记录每一层中出现的最后一个节点。
