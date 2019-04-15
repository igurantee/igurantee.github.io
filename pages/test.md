<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

#### PCA（**<u>P</u>**rincipal **<u>C</u>**omponent **<u>A</u>**nalysis，主成分分析）

##### 1. 问题描述：

*x<sub>1</sub>*, *x<sub>2</sub>*, ... , *x<sub>p</sub>* 为训练样本，其中每个 *x<sub>i</sub>* 均为 *n* 维向量，要求一个 *n×m* 的矩阵 *A*，其将样本 *x<sub>i</sub>* 投影为 *m* 维的向量*y<sub>i</sub>*（其中*m ≤ n*）：

*y<sub>i</sub> = Ax<sub>i</sub>*

达到降低数据集维数，同时保留数据集中对**方差**贡献最大的特征的目的。

##### 2. 几何解释：

可以从两个角度理解 *PCA* 的求解过程（从数学推导中可以看出这两个角度其实是等价的）：

* 最小二乘角度：为了找到数据主要变化方向，需要最小化数据到新特征方向上的距离。

* 方差角度：为了保留对方差贡献最大的特征，需要最大化数据在新特征方向上的投影。

![](https://latex.codecogs.com/gif.latex?f(x)=\frac{1}{\sqrt{2\pi\sigmax}}e^{-\frac{(x-\mu)^{2}}{2\sigma^{2}}})

  

