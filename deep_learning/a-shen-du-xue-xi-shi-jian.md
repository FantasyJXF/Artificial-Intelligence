# 深度学习实践

## Index

* [加速训练的方法](a-shen-du-xue-xi-shi-jian.md#加速训练的方法)
  * [内部方法](a-shen-du-xue-xi-shi-jian.md#内部方法)
  * [外部方法](a-shen-du-xue-xi-shi-jian.md#外部方法)

## 加速训练的方法

### 内部方法

* 网络结构
  * 比如 CNN 与 RNN，前者更适合并行架构
* 优化算法的改进：动量、自适应学习率

  > [./专题-优化算法](https://github.com/FantasyJXF/Artificial-Intelligence/tree/ff40df9ea2a4579767c0a29baed45c578389cd4e/A-深度学习/C-专题-优化算法/README.md)

* 减少参数规模
  * 比如使用 GRU 代替 LSTM
* 参数初始化
  * Batch Normalization

### 外部方法

> [深度学习训练加速方法](https://blog.csdn.net/xuqiaobo/article/details/60769330) - CSDN博客
>
> * GPU 加速
> * 数据并行
> * 模型并行
> * 混合数据并行与模型并行
> * CPU 集群
> * GPU 集群
