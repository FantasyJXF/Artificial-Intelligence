# 算法

## 算法  Algorithm

### **题解**

* [剑指Offer 题解](ti-jie-jian-zhi-offer.md)
* [Leetcode 题解](ti-jie-leetcode.md)

### **专题**

* A
  * [数据结构](https://github.com/FantasyJXF/Artificial-Intelligence/tree/ff40df9ea2a4579767c0a29baed45c578389cd4e/C-算法/专题-A-数据结构/README.md)
  * [数据结构\_Advanced](https://github.com/FantasyJXF/Artificial-Intelligence/tree/ff40df9ea2a4579767c0a29baed45c578389cd4e/C-算法/专题-A-数据结构_Advanced/README.md)
* B
  * [双指针](https://github.com/FantasyJXF/Artificial-Intelligence/tree/ff40df9ea2a4579767c0a29baed45c578389cd4e/C-算法/专题-B-双指针/README.md)
  * [动态规划](https://github.com/FantasyJXF/Artificial-Intelligence/tree/ff40df9ea2a4579767c0a29baed45c578389cd4e/C-算法/专题-B-动态规划/README.md)
* C
  * [排列组合](https://github.com/FantasyJXF/Artificial-Intelligence/tree/ff40df9ea2a4579767c0a29baed45c578389cd4e/C-算法/专题-C-排列组合/README.md)
  * [洗牌、采样、随机数](https://github.com/FantasyJXF/Artificial-Intelligence/tree/ff40df9ea2a4579767c0a29baed45c578389cd4e/C-算法/专题-C-洗牌、采样、随机数/README.md)

### **备忘**

* [IO 模板](bei-wang-io-mo-ban.md)
* [必备算法](bei-wang-bi-bei-suan-fa.md)

### Reference

* f-zyj/[ACM 模板以及个人平时训练的代码](https://github.com/f-zyj/ACM)

  > [ACM 在线模版 - 逐梦者](https://blog.csdn.net/f_zyj/article/details/51594851) - CSDN博客

* [OI Wiki](https://github.com/24OI/OI-wiki/)

### Index

* [排序](./#排序)
  * [稳定排序与不稳定排序](./#稳定排序与不稳定排序)
  * [堆排序-建堆的时间复杂度 `O(N)`](./#堆排序-建堆的时间复杂度-on)
* [Trick](./#trick)
  * [时间复杂度](./#时间复杂度)
  * [敏感空间](./#敏感空间)

## 排序

### 稳定排序与不稳定排序

**稳定排序**

* 冒泡排序、插入排序、归并排序、基数排序

**不稳定排序**

* 选择排序、快速排序、希尔排序、堆排序

### 堆排序-建堆的时间复杂度 `O(N)`

* 堆排序的时间复杂度是 `O(NlogN)` 没有问题
* 但是建堆的时间复杂度是 `O(N)`

  > [为什么建立一个二叉堆的时间为O\(N\)而不是O\(Nlog\(N\)\)?](https://www.zhihu.com/question/264693363/answer/291397356) - 知乎

## Trick

### 时间复杂度

> [百度：ACM trick](https://www.baidu.com/s?wd=ACM%20trick)
>
> * 暴力枚举永远是第一个考虑的方法，但也有一些前提
>   * 如果输入规模 `< 1e4`，那么可以尝试考虑 `O(n^2)` 的算法（两次循环暴力枚举）；如果 `≥ 1e5`，那么可能就需要考虑 `O(nlogn)` 的算法了——这不是绝对的，也可以通过剪枝等操作加速。
>   * \[C++\] string 拼接的速度依次为：1）使用 `stringstream`；2）使用 `append()`；3）使用 `s += c`；4）使用 `s = s + c`——如果有大量拼接操作，要避免使用最后一种方法。

### 敏感空间

> [ACM Trick点&&常用操作记录\(持续更新\)（敏感空间）](https://blog.csdn.net/feynman1999/article/details/79588347) - CSDN博客
>
> * `long long` 上界：`2^63-1 = 9,223,372,036,854,775,807 ≈ 9.223372e+18`
>   * 阶乘：`20! = 2432902008176640000 ≈ 2.432902e+18` OK，`21!`超
>   * Fibnacci 数列：`fib[92] = 7540113804746346429 ≈ 7.540114e+18` OK，`fib[93]` 超
>   * Catalan 数：
>   * 整数划分：
> * **数组大小**：如果内存限制为 2MB，那么最大可开辟的 int 数组为 `2*1024*1024/4 = 524288 ≈ 50,0000`，char 数组为 `2*1024*1024 = 2,097,152 ≈ 200,0000`
>   * 实际单个数组是远开不了那么大，比如 windows 默认的栈好像只有 1MB
>   * 在无法修改栈大小的情况下，可以使用 `new` 或 `malloc` 在**堆**上开辟内存
>
>     ```c
>       int *pa = malloc(sizeof(int)*1024*1024);
>       int *pb = new int[1024*1024];
>     ```
