# MelonHeadsV2.0
MelonHeads algo swap from scrypt to X11
You need three files to in your "MelonHeads" folder to run in windows: the .qt, the .tx, and the .cli.
This coin is now mineable, the blockchain is up and running , here is how to mine:

Open your wallet, and make sure your wallet is connected with a node. 
Your wallet is connected when you see the icon Wallet connections  in the lower right corner of your wallet.
rpcuser=rpc_melonheads
rpcpassword=d21a199a122c1ba136e5ca8aa
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
addnode=72.174.17.145
Open your wallet.

Create a .bat file named mine.bat in the same folder where you extracted melonheads-cli.exe and paste the following text into mine.bat...:
@echo off
set SCRIPT_PATH=%cd%
cd %SCRIPT_PATH%
echo Press [CTRL+C] to stop mining.
:begin
 melonheads-cli.exe generate 1
goto begin 

Save the file.

Execute mine.bat to start mining your first block.
