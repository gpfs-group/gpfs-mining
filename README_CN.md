# GPFS挖矿教程


## Windows 环境
Windows使用GPFS World桌面软件挖矿，它既是GPFS网络节点，也是一个文件管理软件。下载解压运行即可，不需要进行任何配置。  
下载地址： https://github.com/gpfs-group/gpfs-world/releases

软件启动后，会自动生成一个随机的BSC地址，私钥可以复制出来，导入到其他钱包使用。  
也可以使用其他钱包生成的地址，通过修改软件的配置文件实现。配置文件位于repo/config，修改里面的 Wallet.PrivateKey变成你自己的私钥，然后重启软件。


## Linux 环境
下载地址： https://github.com/gpfs-group/gpfs-mining/releases

解压`linux_amd64.zip`，依次执行
```
chmod 766 gpfs
cp gpfs /usr/local/bin
export IPFS_PATH=你想要的工作目录
gpfs daemon --init --miner-address=你的BSC钱包地址
```
linux环境部署前，需要提前生成bsc钱包地址

## 矿工浏览器
https://scan.gpfs.xyz/

可以在矿工浏览器上查看，矿工的状态和出票情况。

## 支票兑换
兑换支票需要跟智能合约交互，所以账号中需要拥有一定数量的BNB作为GAS费。对于windows环境可以在软件上点击“兑换支票”按钮实现，或者在矿工浏览器的兑换支票页面登录MetaMask钱包，点击“兑换支票”。若使用手机钱包，比如TP钱包，也可以将兑换页面复制到钱包中打开直接兑换。


## 挖矿原理

请阅读 [《GPFS白皮书》](https://github.com/gpfs-group/gpfs-litepaper/blob/main/README_CN.md)


## 需要注意的问题
- 每个钱包地址只能给一个节点使用。如果一个地址已经被使用过，系统会忽略该节点。
- P2P网络有一定的延迟性，有时启动后需要等待几分钟才能被其他节点发现。 

## 联系方式

电报群：  https://t.me/gpfs_cn
