# GPFS mining tutorial
[简体中文](README_CN.md)

## Download mining software

Go here to download the latest version of the binary file for the corresponding environment 
https://github.com/gpfs-group/gpfs-mining/releases

## Windows
Unzip `windows_amd64.zip` (32-bit version `windows_386.zip`)  
Open `run.bat` with Notepad, modify the working directory (make sure there is at least 10G space in the hard disk) and wallet address.

```
set IPFS_PATH=The working directory you want
gpfs.exe daemon  --init --miner-address=Your BSC wallet address
pause
```
Then double-click to run `run.bat`, it's that simple.

The last line, the output is as follows, indicating success

```
Daemon is ready
```

## Linux
Unzip `linux_amd64.zip` and execute in turn
```
chmod 766 gpfs
cp gpfs /usr/local/bin
export IPFS_PATH=The working directory you want
gpfs daemon --init --miner-address=Your BSC wallet address
```

## Miner browser
https://scan.gpfs.xyz/

You can check the miner's status and ticket issuance on the miner's browser. Before logging in to MetaMask on the check exchange page, exchange the check into GPS tokens.

## Mining principle
- The GPFS network randomly selects several online lucky miner nodes (detailed in the data amount white paper) every ten minutes. The principle is similar to that of Filecoin.
- Then use the EIP712 signature protocol to generate several checks and issue them to lucky miners. After miners get the check, they need to call the smart contract to exchange the check into GPS tokens. There is no limit to the time to redeem a check, and it can be exchanged in a browser once it has accumulated to a certain amount.
- The total amount of GPS is 10 billion, halved in 4 years, and 23782.3439 GPS will be issued every round (10 minutes) before the halving.
- In each round of tickets issued, 50% will be distributed to lucky miners on average, and 50% will be distributed in proportion to the number of lucky miners holding GPS. Therefore, the more GPS held, the more rewards you will get. (The holding here must be the GPS held in the wallet, which can be transferred from another address or obtained from mining)

## Issues that need attention
- Each wallet address can only be used by one node. If an address has already been used, the system will ignore the node.
- P2P network has a certain delay, sometimes it takes a few minutes to be discovered by other nodes after startup.
- GPFS fully supports all functions and commands of IPFS. You can use `gpfs -h` to view more help.

## Contacts

Telegram： https://t.me/gpfsnet
