# Realtime Pollution Dashboard

A use-case of measuring air quality with sensors around a factory to showcase the ability of Taipy to dashboard streaming data.

<p align="center">
  <img src="media/dashboard.png" alt="Dashboard" width="100%"/>
</p>

## How to use

1. Clone this repository

```bash
git clone https://github.com/Avaiga/demo-realtime-pollution.git
```

2. Install requirements


```bash
pip install -r requirements.txt
```

3. Run the receiver script

```bash
python receiver.py
```

This should open a dashboard in your browser.

4. Run the sender script

```bash
python sender.py
```

This will send data to the dashboard.


## 低空频谱演示demo

1. 通信框架：使用socket传输

2. 变量与接口

需要传输的数据变量名为 outgoing_data
outgoing_data 通过函数update更新
update_interval 为更新频率，单位为秒
receiver 的地址和端口号（本地调试无需修改）
HOST = "127.0.0.1" 
PORT = 65432