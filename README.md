# algorithm00
程序员的算法课之00时间复杂度

1. 算法复杂度
  - 时间复杂度： 执行算法所需要的计算工作量
  - 空间复杂度： 执行算法所需要的内存空间
2. 什么是时间复杂度
  - 在计算机科学中，算法的时间复杂度是一个函数，它定量描述了该算法的运行时间。
  - 以算法输入值规模n为自变量的函数: T(n) = O(f(n))
3. 三种表示时间复杂度的符号，通常用上界，表示不超过
![](ag0-0.png)
4. 大O符号例子
- 如果同时都满足条件，我们需要给出更收敛的答案
![](ag0-1.png)
5. 时间复杂度的比较
![](ag0-2.png)

6. 评价时间复杂度的好坏有3种方式
- 最好情况: 目标值是数组的第一个元素，T(n) = O(1)
- 最坏情况: 目标值是数组的最后一个元素，T(n) = O(n)
- 期望情况(平均情况): T(n) = O(n)
- 一般讨论最坏情况和期望情况

7. 计算时间复杂度-一般问题
- 基本操作的时间复杂度
  - 丢弃常数项
![](ag0-3.png)
  - 上图实际是O(n)
![](ag0-4.png)
  - 上图实际是O(2n),但是丢弃常数项所以即O(n)
  - 丢弃次要项
- 基本操作被执行了多少次（For／While循环）
- 复合操作：加还是乘
  - 假设算法有两步，每一步的时间复杂度为O(A)，O(B)
  - 计算时间复杂度时什么时候该将两步的时间复杂度相加，什么时候该相乘
结论：1. 先做A，然后做完A后， 再做B， 应该将这两件事的时间复杂度相加。2. 每一次做A的时候都需要将B全部做一遍， 应该将这两件事的时间复杂度相乘

8. 一般情况下的算法复杂度例题
- 例题一,O(2n)->O(n)
![](ag0-5.png)
- 例题二,给数组打印出所有的整数对。O(n*n) -> O(n^2)
![](ag0-6.png)
- 例题三
![](ag0-7.png)
- 例题三有两种解法
  - 解法一 
![](ag0-8.png)
  - 解法二
![](ag0-9.png)

9. 递归问题的时间复杂度 
- 什么是递归：在数学与计算机科学中，是指在函数的定义中使用函数自身的方法。递归一词还较常用于描述以自相似方法重复事物的过程。
![](ag0-10.png)
- 以上图中递归为例:
![](ag0-11.png)
- 递归的复杂度由经验看起来通常是O(branches^depth),上图例子中2个分支，深度为n+1曾 ，归一下就是2^n,可以用来判断
- 例题一,算节点一共和是多少  
```java
int sum(Node node){
  if(node == null){
    return 0;
  }
  return sum(node.left) + node.value = sum(node.right);
}
```
- 方法一，根据经验公式
![](ag0-12.png)
- 方法二，用直观的方法，从代码来看
![](ag0-13.png)

- 例题二.计算字符串的全排列
![](ag0-14.png)
- 代码执行过程以字符串'abc'为例
![](ag0-15.png)
![](ag0-16.png)
- 计算复杂度的两种方法
![](ag0-17.png)

- 例题三. 三个小问题，都是求斐波那切数列

![](ag0-18.png)
- 第一个小问题
![](ag0-19.png)
- 第二个小问题
![](ag0-20.png)
- 第三个小问题
![](ag0-21.png)
![](ag0-22.png)

10. 时间复杂度的主定理
![](ag0-23.png)
![](ag0-24.png)
- 面试的时候不要一开始就用主定理，先用之前一般算的方式，然后不经意间表示出我还会主定理计算，就可以展现出自己知识的宽度和广度
![](ag0-25.png)
11. 算法空间复杂度
![](ag0-26.png)

12. 总结
- 算法复杂度
  - 时间复杂度
  - -空间复杂度
- 时间复杂度的概念
  - 概念
  - -3种记号->大O符号
  - -最好／最坏／平均情况
- 时间复杂度的计算
- 一般问题
  - 3大原则：丢弃常数项，丢弃次要项，复合操作
- 递归问题
  - 主定理
- 空间复杂度