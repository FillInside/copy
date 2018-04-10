## Ubuntu安装微信
其实是网页版，做成了客户端，重新登录一次以往的消息全没了。
### 1. 下载微信，去这个网址下载：
    https://github.com/geeeeeeeeek/electronic-wechat/releases
我下的是linux-64.tar.gz
### 2. 解压linux-64.tar.gz
直接解压就行，或者命令行：<br>
    
    sudo tar zxvf linux-x64.tar.gz
### 3. 把解压的文件夹及图标放在/opt下
    sudo mv .../electronic-wechat-linux-x64 /opt/electronic-wechat-linux-x64
    sudo mv .../icon.jpg /opt/electronic-wechat-linux-x64
### 4. 创建终端下的快速启动命令
    sudo ln -s /opt/electronic-wechat-linux-x64/electronic-wechat /usr/bin/electronic-wechat
### 5. 创建快捷方式
    sudo vim /usr/share/applications/wechat.desktop
文本输入：<br>

    [Desktop Entry]
    Encoding=UTF-8
    Version=1.0
    Type=Application
    Name=Electronic WeChat
    Icon=/opt/electronic-wechat-linux-x64/icon.png
    Exec=/opt/electronic-wechat-linux-x64/electronic-wechat
    StartupNotify=false
    StartupWMClass=electronic-wechat
    OnlyShowIn=Unity;
    X-UnityGenerated=true
按ESC，输入:wq即可保存退出
