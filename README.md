### Leetcoder

## Array

## LikedList

## Tree
### 二叉树的遍历
树的便利分为前序/中序/后序，方法分为递归和非递归，总共六种
前序遍历的非递归:
相对于其他两种较为简单，因为每次遍历到一个节点的时候可以直接打印出来，但是需要把右孩子存储起来，并记录左孩子为下一次遍历的对象；

中序遍历，非递归的方法：
依然需要一个辅助栈结构，此外，每次需要打印的节点，其实都会被访问两次，这就需要另一个结构来记录栈中的元素被访问的次数；
可以画图来理清楚思路即可；


## 动态规划

## 回溯算法
要求输出所有可能的解： 用 DFS
要求输出最优的解：    用 DP

比如： 回文子串那一题；


## 贪心算法


## 常规但是需要考虑各种错误情况
### **整数次方问题**
给定一个double类型的浮点数base和int类型的整数exponent。
求base的exponent次方。
需要注意的如下：

- 整数可能是负数
- 底数base是0的情况，需要判断指数是否为0；
  0的0次方无意义，而0的整数次方为0；
- double类型判断是否为0，一般会跟e^6次方，也就是0.0000001比较；=


## 字串问题
题目描述:
设有n个正整数，将他们连接成一排，组成一个最大的多位整数。
如:n=3时，3个整数13,312,343,连成的最大整数为34331213。
如:n=4时,4个整数7,13,4,246连接成的最大整数为7424613。

++solution++
本题可以直接使用字符串比较大小，本来想着直接排序就行了，但其实不行，需要注意到一个问题：
比如12 123， 前两位一样，会导致123比123大，但其实还需要比较那个放在前面。

本题主要是在
> 考察把问题转换为字符串比较大小的问题，需要比较 x+y 和 y+x的大小！！
