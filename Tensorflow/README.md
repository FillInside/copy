## Titan服务器上安装Tensorflow(GPU版）
### 1. 进入实验室Titan服务器
    ssh -p 10022 yehongb@172.18.233.3
### 2. 安装Anaconda
若已安装则忽略这一步<br>
### 3. 搜索当前可用的tensorflow版本
    anaconda search -t conda tensorflow
### 4. 选择一个最新的的GPU版本
比如，选择jjh_cio_testing/tensorflow-gpu的1.0.1版本，输入如下命令查询安装命令：<br>
    
    anaconda show jjh_cio_testing/tensorflow-gpu
### 5.安装
使用最后一行的提示命令进行安装：<br>

    conda install --channel https://conda.anaconda.org/jjh_cio_testing tensorflow-gpu
### 6.查看Tensorflow是否为GPU版本
直接session.run运行个a+b的运算，会有设备初始化的提示<br>
    
    $python
    >>>import tensorflow as tf
    >>>a = tf.constant([1.0, 2.0, 3.0, 4.0, 5.0, 6.0], shape=[2, 3], name='a')
    >>>b = tf.constant([1.0, 2.0, 3.0, 4.0, 5.0, 6.0], shape=[3, 2], name='b')
    >>>c = tf.matmul(a, b)
    >>>sess = tf.Session(config=tf.ConfigProto(log_device_placement=True))
    >>>print(sess.run(c))
若看到输出有“GPU:0”等，则表示所装Tensorflow微GPU版<br>
### 7.参考
    https://www.cnblogs.com/willnote/p/6746499.html
    https://www.zhihu.com/question/263850405
