# 第六周总结

## 单词搜索II复杂度分析

假设board长度m*n，words单词数j, 单词长度k
用trie实现的情况下：

1. 把words加入字典 j*k
2. 递归加board遍历 m*n*4^k（最坏，且没有剪枝的情况）。

由于我们提前做了判断和剪枝，所以真实复杂度会比这个好很多。
所以最坏时间复杂度为: O(j*k + m*n*4^k)
最好时间复杂度为: O(j*k + m*n*k)

### Trie树

> 字典树、单词查找树、键树
> trie树核心思想是空间换时间

应用：

* 统计和排序大量的字符串
* 搜索引擎文本词频统计

优点：最大限度地减少无谓的字符串比较，查询效率比哈希表高

### 并查集

使用场景

* 组团、配对问题
* 判断分组

### 高级搜索

* 剪枝
* 双向BFS
* 启发式搜索（`A*`）

### 红黑树&AVL树

平衡树

AVL树
> 平衡因子（Balance Factor）：
> 他的左子树的高度减去它的右子树的高度（有时相反）左右子节点差不超过绝对值1
> balance factor = {-1, 0, 1}

旋转

1. 左旋
2. 右旋
3. 左右旋
4. 右左旋

红黑树
红黑树是一种近似平衡的二叉搜索树(Binary Search Tree)，它能够确保任何一 个结点的左右子树的高度差小于两倍。
