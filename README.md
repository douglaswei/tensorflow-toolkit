# tensorflow-toolkit

### 目的
1. tf的学习笔记，其中包括自学习过程中的问题&解答
2. 从自己的视角梳理学习的体系，并梳理sample
3. 在一定程度上构建tf-api的封装，tf内部有不少高级的封装，但目前看来都不及prettyTesor，未来Google可能有出一套封装的API，所以这一块需要，但不确定性比较大


### Lower API
##### Basic 
1. mnist CNN 网络构建
2. tensor board
3. parameters

[code](LowerAPI/1.1_mnist_cnn.ipynb)

#### random_normal vs truncated_normal
```
作为tensorflow里的正态分布产生函数，这两个函数的输入参数几乎完全一致，
而其主要的区别在于，tf.truncated_normal的输出如字面意思是截断的，而截断的标准是2倍的stddev。

举例，当输入参数mean = 0 ， stddev =1时，
使用tf.truncated_normal的输出是不可能出现[-2,2]以外的点的，
而如果shape够大的话，tf.random_normal却会产生2.2或者2.4之类的输出。

```

##### Model & serving
- Saver and Model

[官方文档](https://www.tensorflow.org/programmers_guide/saved_model)
[code](LowerAPI/1.2_saver_model.ipynb)

```
Estimator 会自动保存变量;
Saver 提供save、restore方法来保存、加载Graph(graph的概念是:多个运算之间的依赖关系)
tf.train.Saver() 默认存储graph中的所有变量，每个变量存储的name是变量创建时赋予的name


```

- run the model as service


##### distributed TensorFlow(TODO)
[官方文档](https://www.tensorflow.org/deploy/distributed)
  

5. ensemble-运行多轮训练，尝试不同的训练效果，最后多个模型共同决策，好像boostrap/bagging
6. embedding
7. multi-gpu
8. saver.save(session,path) 保存多次 会怎样？saver.restore(session,path), save后的每个文件的作用，包括ckpt
9. Optimizer 比较
10. parameter server
11. transfer learning 中trainable参数，前几层网络结构&参数不变，后面结构|参数都可以改变，实现的技巧
12. tfRecords & datasets
13. metadata
14. balboa_scope(activation_fn = tf.nn.relu)
15. Inception model project的使用，以及bottle net 的使用（transfer learning）
16. sklearn.decompostion vs sklearn.manifold.TSNE
17. 不同分类之间的学习率，sklearn.utils.class_weight.compute_class_weight
18. session.run返回值是啥？

### Higher API
- tflearn
- tf.layer
- tf.contrib.laysers
- tf.contrib.slim
- tf.contrib.learn
- tf.Estimator
- keras
- PrettyTensor
- 超参-调参
    1. scikit-optimize
    2. sklearning的方法
    3. h5py
- 开源项目

### 理论
- deep learning 如何做回归
- deep learning & reinforcement learning
- deep dream
- Dropout
