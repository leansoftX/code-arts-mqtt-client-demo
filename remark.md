## 本地运行
- 本地环境参考这个：https://www.cnblogs.com/CltCj/articles/17661086.html
- 在线ide 已经有编译环境了：https://810aa9f7.lightly.teamcode.com/ 
- 安装依赖：
```
git clone https://github.com/eclipse/paho.mqtt.c.git
cd paho.mqtt.c
mkdir build
cd build
cmake ..
make 
make install
```
- 点在线ide的运行按钮 
- 或者命令行手动编译运行
```
mkdir manual-build && cd manual-build
cmake .. && make  ##构建 
cd .. && chmod -R 777 manual-build ##添加执行权限
cd manual-build
./mqtt_c  ## 运行 crtl+C 退出

- 程序会订阅主 vehicle-warning 消息
- 程序会循环发布主题 vehicle-info, 会发两个，一个是读取vehicle-info.json文件的内容，一个是同样格式的静态内容

- 使用 http://www.emqx.io/online-mqtt-client 接收和发送消息以验证上面两个主题的消息



