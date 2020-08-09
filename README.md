### Tutorial how to mine MAZE SLP token on Android phone with Linux Ubuntu emulator

_v1.0 created by [B_S_Z](https://t.me/b_s_z)_

[MAZE](https://mazetoken.github.io) is based on [Mistcoin](https://mistcoin.org)

We can use 3 different miners ([Kasumi's](https://mistcoin.org), [Kasumi's original version compiled by Blockparty-sh and team](https://github.com/blockparty-sh/mist-miner) and [Blue's miner](https://gitlab.com/blue_mist/miner))

Read [here](https://github.com/blockparty-sh/mist-miner) how to prepare your Electron Cash wallet (SLP edition) for mining

_You can also mine Mist_

_You can use a spare phone_

_You can restart your phone first_

### Go to Google Play Store and download UserLAnd app

- Install the app

- Open the app and install Ubuntu

- Setup your username and passwords

- Choose SSH

### Run commands:

sudo apt-get update && sudo apt-get dist-upgrade

sudo apt-get install git

sudo apt-get install wget

sudo apt-get install curl

curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -

sudo apt-get install - y nodejs

sudo apt-get install gcc g++ make

sudo npm install -g npm@latest

sudo apt-get install nano

sudo apt-get install zip unzip

### Create a new directory e.g. miner, download and unpack the selected miner:

mkdir miner

cd miner

wget https://github.com/mazetoken/miners/raw/master/maze-kasumi-bchd-miner.zip

- _You can also try other miners:_

_wget https://github.com/mazetoken/miners/raw/master/maze-kasumi-JT-miner.zip_

or 

_wget https://github.com/mazetoken/miners/raw/master/maze-blue-miner.zip_

or Mist miner

_wget https://github.com/mazetoken/miners/raw/master/mist-kasumi-bchd-miner.zip_

unzip maze-kasumi-bchd-miner.zip

- _maze-kasumi-bchd-miner directory will be created (or unzip other miner you have downloaded)_

### Download CMake to miner directory (because we need a new version of CMake for fastmine ; no need to do this for Blue's miner):

sudo apt install build-essential libssl-dev

wget https://github.com/Kitware/CMake/releases/download/v3.16.5/cmake-3.16.5.tar.gz

tar -zxvf cmake-3.16.5.tar.gz

### Navigate to cmake directory:

cd cmake-3.16.5

### Run commands:

- _*unfortunately, it will take some time - about two hours, so be patient; You can change the sleep time of your phone's display to 30 minutes to make it a little faster; you can skip this if you don't want to mine with fastmine):_

./bootstrap

make 

sudo make install

### Navigate to maze-kasumi-bchd-miner directory (or other miner directory):

cd ..

cd maze-kasumi-bchd-miner

### Open .env in Nano editor:

sudo nano .env

- _Type/paste your WIF=" ..." (right click on your addres in Electron Cash wallet to get a private key)_

- _You can change your tag in MINER_UTF8="..."_

- _You can change FASTMIE to "yes" (leave empty or type "no" if you don't want to mine with fastmine)
and then tap ctrl O enter - to save changes and ctrl X enter - to exit editor_

### Navigate to fastmine directory and run cmake (you can skip this if you don't want to mine with fastmine):

cd fastmine

cmake . && make

### Navigate to maze-kasumi-bchd-miner (or other miner directory), install and start the miner:

cd ..

npm i

_Do not run npm audit fix !_

npm start

- _Tap Ctrl C (to stop the miner)_

- _Start miner again (if you have closed UserLAnd app):_

cd miner

cd maze-kasumi-bchd-miner

npm start

### Join [MAZE](https://t.me/mazemining) Telegram group

_I will update this tutorial if I find bugs or improvements_

Have fun
