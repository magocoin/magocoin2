# Magocoin COIN

* Ticker: magocoin
* Algorithm: X11
* Masternode colletral: 1000 magocoin
* Masternode rewards: 85%
* Block reward: 14-21-7 magocoin
* POS start block: 1200
* Block Timer: 60 seconds
* Maturity: 15 blocks
* Premine: 30 000 magocoin
***

## VPS installation
Shell script to install a [Eclipse Masternode](https://magocoinad.network/) on a Linux server running Ubuntu 16.04.
Use it on your own risk.
```
wget -N https://github.com/magocoinadnetwork/magocoin/releases/download/v3.0.0.1/magocoin-3.0.0-installer.sh
bash magocoin-3.0.0-installer.sh
```
***

## Desktop wallet setup

After the Masternode is up and running, you need to configure the desktop wallet accordingly. Here are the stmagocoin:
1. Open the Eclipse Desktop Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **1000** magocoin to **MN1**. You need to send all 1000 coins in one single transaction.
4. Wait for 15 confirmations.
5. Go to **Help -> "Debug Window - Console"**
6. Type the following command: **masternode outputs**
7. Go to  **Tools -> "Open Masternode Configuration File"**
8. Add the following entry:
```
Alias Address Privkey TxHash TxIndex
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* TxIndex:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is unlocked.
12. Open **Debug Console** and type:
```
startmasternode alias 0 MN1
```
13. Login to your VPS and check your masternode status by running the following command to confirm your MN is running:
```
magocoin-cli masternode status
```
***

## Usage:
```
magocoin-cli masternode status #To check your MN status
magocoin-cli getinfo #To get general info such as Eclipse version and current block numnber
magocoin-cli mnsync status #To check if your MN is synced.
```
***

## Source
Based on:
https://github.com/zoldur/Masternode-setup-guide/blob/master/README.md
