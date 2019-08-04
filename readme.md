![](/logo.png)

# HSPMiner

Nvidia GPU Miner for `Bytom(比原链)`mining.

## Download

[Download here](https://github.com/hspminer/HSPMinerBTM/releases)

## Community support

QQ： 870349675

## Performance (stock frequency)

| Algorithm        |  Coin   | P106-100  |  P104-8G   |  1070ti  |  1080ti  |   2080   |
| :--------------- | :-----: | :-------: | :--------: | :------: | :------: | :------: |
| tensority        |   BTM   |   1,900   |    3000    |  3,400   |  5,000   |  11,500  |


## Features

* Support Windows & Linux.
* Support backup mining pool configuration.
* Support SSL connection to mining pools.
* Dev Fee: 
  * tensority_ethash


## Requirements

- win7,win10,Linux
  - Nvidia, 10 series graphics cards, such as 1030, 1050, 1060, 1070, 1080, 1080ti
  - Nvidia driver version >398

- GPU Specific Requirements:

|    Algorithm     |  Coin   | Compute Capability | Memory (Win7 & Linux) | Memory (Win10) |
| :--------------: | :-----: | :----------------: | :-------------------: | :------------: |
|    tensority     |   BTM   |   6.1, 7.0, 7.5    |          1GB          |      1GB       |


#How to use
- Windows system
  - Open the run.cmd file with Notepad
  - Replace wallet address after -bwal
  - (Optional) Replace the as-built name after -bworker (usually used to distinguish machines)
  - (Optional) Replace the pool address and port behind -bpool
  - (Optional) Replace the password for the connection pool behind -bpsw
  - Save, click to start run.cmd
  - (Optional) Click WebMonitor.cmd to launch the browser (or launch the browser directly) to view the mining status (in the presence of the -api parameter)

- Linux system
  - Open the run.sh file with a text editor
  - Replace wallet address after -bwal
  - (Optional) Replace the as-built name after -bworker (usually used to distinguish machines)
  - (Optional) Replace the pool address and port behind -bpool
  - (Optional) Replace the password for the connection pool behind -bpsw
  - Save, console run. /run.sh
  - (Optional) WebMonitor.sh launches the browser (or launches the browser directly) to view the mining status (in the presence of the -api parameter)


## Sample Usages

#### BTM

- **f2pool:** HSPMiner.exe -bpool btm.f2pool.com:9221 -bwal bm1q43kya8xnmfas5pk79nhhnj7656g0jxwn9mdgyq -bworker default -bpsw passd -logfile -api 127.0.0.1:16666


## CMD options：
-	-bwal		The Bytom Wallet Address
-	-bworker	The worker name of Bytom
-	-bpool		The Bytom pool address, add tls://pool_url:port to enable TLS connection
-	-bpsw		The Bytom mine password
-	-bdevice	Dig the devices enabled by Bytom. The default is all devices. You can use -bdevice 0, 2, 4 to limit the operation on GPU0, 2, and 4.

##Run information:
-	-api		Enable the network monitoring address, such as: 192.168.1.2:16666, use the browser to access http://192.168.1.2:16666, monitor the mining machine operation
-	-logfile	Enable the log file, the default is to generate the file name according to the time, followed by the file name to specify the file, such as -logfile hspminer.log
-	-hide		Hide the interface immediately after starting the program, note that it will run in the background. If you open the api interface, you can click WebMonitor.cmd to start the browser monitoring (not available under Linux)

### Web Monitor

Open http://api_host:port/ in your browser to use web monitor.


## Change Log

#### HSPMinerBTM 2.0.1 2019/1/16

- Fix:Fix some bugs

