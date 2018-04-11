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
