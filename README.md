git clone -b manyuser https://github.com/ToyoDAdoubi/shadowsocksr.git

https://doub.io/ss-jc11/

https://doub.io/ss-jc10/



服务端配置
进入根目录：
cd shadowsocksr
初始化配置：

bash initcfg.sh
通过配置文件运行
打开并修改配置文件，根据下下面的各选项说明来修改各个参数。

vi user-config.json


SSH 登录，sudo -i 切换到 root 用户。方法源自秋水逸冰：https://teddysun.com/489.html

运行以下命令：

wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh
chmod +x bbr.sh
./bbr.sh

安装完成后，脚本会提示需要重启 VPS，输入 y 并回车后重启。

重启完成后，进入 VPS，验证一下是否成功安装最新内核并开启 TCP BBR，输入以下命令：

uname -r

查看内核版本，含有 4.11 就表示 OK 了

sysctl net.ipv4.tcp_available_congestion_control

返回值一般为：

net.ipv4.tcp_available_congestion_control = bbr cubic reno
