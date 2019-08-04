![](/logo.png)

# HSPMiner

用于显卡GPU的`Bytom(比原链)`挖矿软件。

## 下载地址

[从这里下载](https://github.com/hspminer/HSPMinerBTM/releases)

## 社区支持

官方QQ群： 870349675

## 参考算力（默认频率）

| 算法             |  币种   | P106-100  |  P104-8G   |  1070ti  |  1080ti  |   2080   |
| :--------------- | :-----: | :-------: | :--------: | :------: | :------: | :------: |
| ...           |   ...   |   ...   |   ...    |  ...   |   ...   |   ...    |


## 功能特点

- 支持Windows和Linux
- 支持备用矿池的设置
- 支持SSL方式连接矿池
- 开发手续费:
  - 


## 配置需求

- win7,win10,Linux系统
  - Nvidia,10系列显卡,比如1030,1050,1060,1070,1080,1080ti
  - Nvidia 驱动版本>398

- 显卡参数需求:

|       算法       |  币种   | Compute Capability | 显存 (Win7 & Linux) | 显存 (Win10) |
| :--------------: | :-----: | :----------------: | :-----------------: | :----------: |


#使用方法
- Windows系统
  - 使用记事本打开run.cmd文件
  - 替换-bwal 后的钱包地址
  - (可选)替换-bworker 后的旷工名称(一般用于区分机器)
  - (可选)替换-bpool 后面的矿池地址和端口
  - (可选)替换-bpsw 后面的连接矿池的密码
  - 保存,点击启动run.cmd
  - (可选)点击WebMonitor.cmd启动浏览器(或直接启动浏览器),可查看挖矿状态(-api参数存在情况下)
- Linux系统
  - 使用文本编辑器打开run.sh文件
  - 替换-bwal 后的钱包地址
  - (可选)替换-bworker 后的旷工名称(一般用于区分机器)
  - (可选)替换-bpool 后面的矿池地址和端口
  - (可选)替换-bpsw 后面的连接矿池的密码
  - 保存,控制台运行./run.sh
  - (可选)WebMonitor.sh启动浏览器(或直接启动浏览器),可查看挖矿状态(-api参数存在情况下)


## 使用样例

#### BTM

- **f2pool:** HSPMiner.exe -bpool btm.f2pool.com:9221 -bwal  {替换钱包地址} -bworker {替换旷工名称} -bpsw {替换密码} -logfile -api 0.0.0.0:16666

## 命令行参数
-	-bwal		挖Bytom钱包地址
-	-bworker	挖Bytom旷工名称
-	-bpool		挖Bytom矿池地址,可加tls://pool_url:port,启用TLS连接
-	-bpsw		挖Bytom矿池密码
-	-bdevice	挖Bytom启用的设备,默认为全部设备,可用-bdevice 0,2,4来限制只在GPU0,2,4上运行

##运行相关:
-	-api		启用网络监控的地址,比如:192.168.1.2:16666,可用浏览器访问http://192.168.1.2:16666,监控矿机运行
-	-logfile	启用log文件,默认为根据时间生成文件名称,后面可跟文件名称来指定文件,比如-logfile hspminer.log
-	-hide		启动程序后立即隐藏界面,注意会在后台运行,如果开了api接口，可点击WebMonitor.cmd启动浏览器监控(Linux下不可用)

## API查询接口

### 网页监控

在浏览器中打开 http://api_host:port/ 启动网页监控.


## FAQ


#### 为什么我的矿池算力比本地算力低?

- `矿池的显示算力`


## 修改记录

#### HSPMinerBTM 2.0.1 2019/1/16

- Fix:修正一些bug

