# MelonHeadsV2.0
MelonHeads algo swap from scrypt to X11
This coin is now mineable, the blockchain is up and running , here is how to mine:

Getting started for Raspberry Pi
Use the following instructions to mine a block.

Open your wallet, and make sure your wallet is connected with a node. 
Your wallet is connected when you see the icon Wallet connections X11 in the lower right corner of your wallet.

The message “Syncing Headers (0,0%)” will disappear once you mine your first block.

Close your wallet and create the file melonheads.conf in the folder “$HOME/.melonheads/”.

Paste the following text into melonheads.conf and save the file.

rpcuser=rpc_melonheads
rpcpassword=e24d93e522d58354fa545f110
rpcallowip=127.0.0.1
rpcport=4217
listen=1
server=1
addnode=node1.walletbuilders.com

Open your wallet.

Create a file named mine.sh and paste the following text into mine.sh.

#!/bin/bash
SCRIPT_PATH=`pwd`;
cd $SCRIPT_PATH
echo Press [CTRL+C] to stop mining.
while :
do
 melonheads-cli generate 1
done 

Save the file.

Open the terminal on your Raspberry Pi.

Go to the directory where you extracted melonheads-qt.

E.G. cd Downloads

Execute the following command in Terminal to make mine.sh executable.

chmod +x mine.sh

Execute the following command in Terminal to start mining your first block.

./mine.sh
