# tensorflow-toolkit

### 目的
1. tf的学习笔记，其中包括自学习过程中的问题&解答
2. 从自己的视角梳理学习的体系，并梳理sample
3. 在一定程度上构建tf-api的封装，tf内部有不少高级的封装，但目前看来都不及prettyTesor，未来Google可能有出一套封装的API，所以这一块需要，但不确定性比较大


### Lower API
1. mnist CNN 网络构建
2. tensor board
3. random_normal vs turncated_noarmal
4. tensorFlow Cloud
5. ensemble - 运行多轮训练，尝试不同的训练效果，最后多个模型共同决策，好像boostrap/bagging
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
19. 


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
