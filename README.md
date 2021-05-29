# GPFS挖矿教程

#### GPFS将于2021年6月1日开启正式网挖矿，目前挖的是测试币，没有任何价值，请不要兑换支票。。。。

## 下载挖矿软件

到这里下载对应环境的最新版本二进制文件  
https://github.com/gpfs-group/gpfs-mining/releases

## Windows 环境
解压`windows_amd64.zip`
用记事本打开`run.bat`, 修改其中的工作目录（保证硬盘中至少有10G空间）和钱包地址。
```
set IPFS_PATH=你想要的工作目录
gpfs.exe daemon  --init --miner-address=你的BSC钱包地址
pause
```
然后双击运行`run.bat`，就这么简单。

最后一行，输出如下，表示成功了
```
Daemon is ready
```

## Linux 环境
解压`linux_amd64.zip`，依次执行
```
chmod 766 gpfs
cp gpfs /usr/local/bin
export IPFS_PATH=你想要的工作目录
gpfs daemon --init --miner-address=你的BSC钱包地址
```

## 矿工浏览器
https://scan.gpfs.xyz/

可以在矿工浏览器上查看，矿工的状态和出票情况。在兑换支票页面登录MetaMask前，将支票兑换成GPS代币。


## 挖矿原理
- GPFS网络每十分钟随机选出若干个（数据数量白皮书中有详细说明）在线的幸运矿工节点。其原理类似Filecoin的爆块。
- 然后使用EIP712签名协议，生成若干张支票，发放给幸运矿工。矿工得到支票后，需要调用智能合约，将支票兑换成GPS代币。兑换支票的时间没有限制，可积累到一定数量后在浏览器中一次性兑换。
- GPS总量100亿，4年减半，减半前每轮（10分钟）出票 2378.2343 GPS。
- 每轮出票，50%平均发放给幸运矿工，50%按幸运矿工持有GPS的数量比例发放，所以持有GPS数量越多，获得奖励越多。（这里的持有必须是钱包中持有的GPS，可以是从其他地址转账过来，或者挖矿兑换得来）


## 需要注意的问题
- 每个钱包地址只能给一个节点使用。如果一个地址已经被使用过，系统会忽略该节点。
- P2P网络有一定的延迟性，有时启动后需要等待几分钟才能被其他节点发现。 
- GPFS完全支持IPFS的所有功能和命令，可以通过 `gpfs -h`，查看更多帮助。

## 联系方式

电报群：  https://t.me/gpfs_cn
