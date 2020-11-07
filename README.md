## MAZE mining environment and tutorial
### MAZE is a mineable, proof-of-work SLP token based on [Mistcoin](https://mistcoin.org/)

_scroll down for mining tutorial_

MAZE Token id: bb553ac2ac7af0fcd4f24f9dfacc7f925bfb1446c6e18c7966db95a8d50fb378

MAZE Token covenant contract script environment:
- MINER_COVENANT_V1="5779820128947f777601207f75597982012c947f757601687f777678827758947f7576538b7f77765c7982777f011179011179ad011179828c7f756079a8011279bb011479815e7981788c88765b79968b0114795e795279965480880400000000011579bc7e0112790117797eaa765f797f757681008854011a797e56797e170000000000000000396a04534c50000101044d494e54200113797e030102087e54797e0c22020000000000001976a914011879a97e0288ac7e0b220200000000000017a9145379a97e01877e527952797e787eaa607988587901127993b175516b6d6d6d6d6d6d6d6d6d6d6d6d6d6d6d6c"
- TOKEN_INIT_REWARD_V1=800000000
- TOKEN_HALVING_INTERVAL_V1=4320
- MINER_DIFFICULTY_V1=3
- TOKEN_START_BLOCK_V1=645065
- TOKEN_ID_V1="bb553ac2ac7af0fcd4f24f9dfacc7f925bfb1446c6e18c7966db95a8d50fb378"

_MINER_COVENANT_V1 is a template and can be used for every mineable tokens based on Mist_

### MAZE Reward Schedule:

Token Height | MAZE Reward

1-4319 | 800

4320-8639 | 400

8640-12959 | 266,666666

12960-17279 | 200

17280-21599 | 160

21600-25919 | 133,333333

25920-30239 | 114,292929

30240-34559 | 100

34560< | ...

MAZE covenant contract script before removing dummy variables and nips not optimized -
0511111111110a33333333333333333333040008af2f5302e01003c9d7095779820128947f777601207f75597982012c947f757601687f777678827758947f7576538b7f77765c7982777f011179011179ad011179828c7f756079a8011279bb011479815e7981788c88765b79968b0114795e795279965480880400000000011579bc7e0112790117797eaa765f797f757681008854011a797e56797e170000000000000000396a04534c50000101044d494e54200113797e030102087e54797e0c22020000000000001976a914011879a97e0288ac7e0b220200000000000017a9145379a97e01877e527952797e787eaa607988587901127993b17551777777777777777777777777777777777777777777777777777777777777

MAZE covenant contract script before removing dummy variables and nips optimized -
0511111111110a33333333333333333333040008af2f5302e01003c9d7095779820128947f777601207f75597982012c947f757601687f777678827758947f7576538b7f77765c7982777f011179011179ad011179828c7f756079a8011279bb011479815e7981788c88765b79968b0114795e795279965480880400000000011579bc7e0112790117797eaa765f797f757681008854011a797e56797e170000000000000000396a04534c50000101044d494e54200113797e030102087e54797e0c22020000000000001976a914011879a97e0288ac7e0b220200000000000017a9145379a97e01877e527952797e787eaa607988587901127993b175516b6d6d6d6d6d6d6d6d6d6d6d6d6d6d6d6c

MAZE [Telegram group](https://t.me/mazemining)

_MAZE TOKEN 2020, created by [B_S_Z](https://t.me/b_s_z)_


## Tutorial - how to mine MAZE SLP token (or other tokens) on Windows or Android phone

_v.5.0_

mazebchdminer is a version of Mist miner - [bchd_mist_miner_v1](https://mistcoin.org), prepared for mining [MAZE](https://mazetoken.github.io) and patched for BigNumber error and [dust input attack](https://gitlab.com/blue_mist/miner/-/commit/e64b1440619589483c3b38870e5cafb791448045)

_You can try to install and mine with [mminer 1.0.0](https://github.com/mazetoken/mminer) - updated version of (bchd_mist_miner_V1 and mazebchdminer). Tutorial is the same. I've updated npm packages and generateV1.ts - support for slpjs v.0.27.8 and grpc-bchrpc-node v.0.11.3. You need npm@7.0.6 for mminer. No guarantee that mminer will be faster than mazebchdminer, but from now I will only work with mminer (mazebchdminer won`t be updated)._

You can mine other tokens (Mist, dSLP, BTCL) with mazebchminer (or mminer) too. To do this you need to:

- change .env file in mazebchdminer folder for [other token environment](https://github.com/mazetoken/mining/raw/master/tokensenv.zip)

- delete .cache file from mazebchdminer folder,

- delete cache.js and cache.js.map files from mazebchdminer src folder (if you have node_modules already installed in mazebchdminer folder)

_Before you start mining other tokens you can paste .cache file for the token you want to mine to speed up downloading txid (token txid are stored in .cache file; make sure that there is a dot before cache file name)_

_You can get .cache files for different tokens from [here](https:/github.com/mazetoken/mining/raw/master/tokenscache.zip)_

### Prepare your Electron Cash SLP desktop wallet for mining

- Download [Electron Cash SLP wallet](https://simpleledger.cash/project/electron-cash-slp-edition/)

- Create two wallets in Electron Cash, e.g. wallet_1 (mining wallet) and wallet_2 (funding wallet)

- Open wallet_2 (funding wallet), choose an address and send some BCH (e.g. 0.00025000) to this address

- Open wallet_1 (mining wallet), choose your mining address for your mining coins (0.00001870). Send, to the mining address, from wallet_2, multiple 0.00001870 BCH in one transanction e.g. - paste in send tab - pay to field: 

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

simpleledger:yourminingaddress,0.00001870

_... - you can add more_

_* in BCH amount field you can type e.g. 0.00000600_

- Right click on your mining address (in wallet_1) and get your private key (WIF)

_* Don't send other BCH to your mining address, otherwise you could pay high fee or you won't mine anything_

### Mining on Windows

Two methods to install the miner. If you have some issues or questions feel free to ask https://t.me/mazemining)

#### 1 method:

- Download [mazebchdminer.zip](https://github.com/mazetoken/mining/raw/master/mazebchdminer.zip) and unzip it. Copy mazebchdminer folder to drive C. Open the folder and open .env file in notepad. Paste your WIF in .env. If you want you can try to set BCHD_GRPC_URL="bchd.imaginary.cash:8335" in .env (no need to do this - default BCHD_URL can be empty). Save the file

_If you want to try mminer download [mminer](https://github.com/mazetoken/mminer) - click green button - download .zip_

- Open Windows Control panel - go to "Programs" - go to "Turn Windows features on or off" - select "Windows Subsystem for Linux" and check the box, click ok and reboot Windows

- Download and install Ubuntu 20.4 LTS from Microsoft Store (type ubuntu in search bar)

- Open Ubuntu command line (Start menu - Ubuntu)

- Setup your username and password

- Type commands:

cd /mnt/c

sudo apt update

sudo apt upgrade

sudo apt-get install git gcc g++ make

cd mazebchdminer

cd fastmine

cmake . && make

cd ..

npm i

_* Ignore errors. Do not run npm audit fix!_

npm start

_* to stop the miner press Ctrl C_

#### 2 method:

- Make sure that Microsoft Visual C++ Redistributable is installed on your system. If it`s not, you can download it from [here](https://aka.ms/vs/16/release/VC_redist.x86.exe) and [here](https://aka.ms/vs/16/release/VC_redist.x64.exe) - you need to install both

- Download and install [Nodejs](https://nodejs.org/en/) 14.15.0

- Download and install [Git](https://gitforwindows.org/)

- Download [mazebchdminer.zip](https://github.com/mazetoken/mining/raw/master/mazebchdminer.zip) and unzip it. Copy mazebchdmazeminer folder to drive C. Open the folder and open .env file in notepad. Paste your WIF in .env. If you want you can try to set BCHD_GRPC_URL="bchd.imaginary.cash:8335" in .env (no need to do this - default BCHD_URL can be empty). Save the file. If you run multiple instances on the same pc/laptop BCHD_GRPC_URL should be the same for every instance

- Open Windows PowerShell (Windows X) and type commands:

cd ..

cd  ..

cd mazebchdminer

npm i -g npm@7.0.6 _(do this only once - npm will be updated globally; don`t update to npm@7.0.9)_

npm i

_* Do not run npm audit fix !_

npm start

_* to stop the miner press Ctrl C and type Y_

### Mining on Android phone

_* You will need 2GB ram in your phone_

Go to Google Play Store and download UserLAnd app

- Install the app

- Open the app and install Ubuntu

- Setup your username and passwords

- Choose SSH

### Type commands:

sudo apt-get update && sudo apt-get dist-upgrade

sudo apt-get install git

sudo apt-get install wget

sudo apt-get install curl

curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -

sudo apt-get install -y nodejs

sudo apt-get install npm

sudo apt-get install gcc g++ make

sudo apt-get install nano

sudo apt-get install zip unzip

### Create a new directory e.g. miner, download and unpack the miner:

mkdir miner

cd miner

wget https://github.com/mazetoken/mining/raw/master/mazebchdminer.zip

unzip mazebchdminer.zip

_mazebchdminer directory will be created_

_If you want to try mminer type: git clone https://github.com/mazetoken/mminer.git_

### Download CMake to miner directory (because we need a new version of CMake for fastmine):

sudo apt install build-essential libssl-dev

wget https://github.com/Kitware/CMake/releases/download/v3.16.5/cmake-3.16.5.tar.gz

tar -zxvf cmake-3.16.5.tar.gz

### Navigate to cmake directory:

cd cmake-3.16.5

### Run commands:

_* unfortunately, it will take some time - about two-three hours, so be patient; You can change the sleep time of your phone's display to 30 minutes to make it a little faster; you can skip this if you don't want to mine with fastmine; no need to use fastmine for mining dSLP token):_

./bootstrap

make 

sudo make install

### Navigate to mazebchdminer directory:

cd ..

cd mazebchdminer

### Open .env in Nano editor:

sudo nano .env

- _Type/paste your WIF=" ..." (right click on your addres in Electron Cash wallet to get a private key)_

- _Type/paste other token environment if you want to mine other mineable tokens_

- _You can type your tag in MINER_UTF8="..."_

- _You can change FASTMIE to "no" (if you didn`t install fastmine)

- _Tap: ctrl O enter - to save changes and ctrl X enter - to exit editor_

### Navigate to fastmine directory and run cmake (you can skip this if you don't want to mine with fastmine):

cd fastmine

cmake . && make

### Navigate to mazebchdminer, install and start the miner:

cd ..

npm i

_* Ignore errors. Do not run npm audit fix !_

npm start

- _Tap Ctrl C (to stop the miner)_

- _Start miner again (if you have closed UserLAnd app):_

cd miner

cd mazebchdminer

npm start



_I will update this tutorial if I find bugs or improvements_

Have fun

_B_S_Z_
