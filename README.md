# Realtime Pollution Dashboard

A use-case of measuring air quality with sensors around a factory to showcase the ability of Taipy to dashboard streaming data.

<p align="center">
  <img src="media/dashboard.png" alt="Dashboard" width="100%"/>
</p>

## 低空频谱演示demo

1. 通信框架：使用socket传输

2. 变量与接口

sender端：

需要传输的数据变量名为 outgoing_data

outgoing_data 通过函数update更新

update_interval 为更新频率，单位为秒

receiver 的地址和端口号（本地调试无需修改）
HOST = "127.0.0.1" 
PORT = 65432

receiver端：
通过pollutions = pickle.loads(data) 将传输的数据，解包变为原来的数据。


## 使用方法

1. Clone this repository

```bash
git clone https://github.com/git-winnermianqian/demo_1.git
```

2. Install taipy


```bash
pip install taipy
```


3. Run the receiver script

```bash
python receiver.py
```

Open th dashboard in your browser. http://127.0.0.1:5000

4. Run the sender script

```bash
python sender.py
```

This will send data to the dashboard.

p.s.
from https://github.com/Avaiga/demo-realtime-pollution.git
