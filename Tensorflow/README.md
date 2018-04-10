## Titan服务器上安装Tensorflow
### 1. 进入实验室Titan服务器
    ssh -p 10022 yehongb@172.18.233.3
### 2. 用pip安装
    pip install --upgrade tensorflow
### 3. 测试代码
    $ python
    >>> import tensorflow as tf
    >>> hello = tf.constant('Hello, TensorFlow!')
    >>> sess = tf.Session()
    >>> print sess.run(hello)
    Hello, TensorFlow!
