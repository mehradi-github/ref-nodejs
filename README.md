# Installing Node.js
Installing Node.js using Linux Command Line.

- [Installing Node.js](#installing-nodejs)
  - [Installing Node.js using Linux Binaries (x64)](#installing-nodejs-using-linux-binaries-x64)
  - [Installing Node.js from source code](#installing-nodejs-from-source-code)



## Installing Node.js using Linux Binaries (x64)

Download the NodeJS [Linux Binaries (x64)] : https://nodejs.org/en/download/

```sh
sudo mkdir /usr/local/lib/node
sudo tar -xJvf node-v18.16.0-linux-x64.tar.xz
sudo mv ./node-v18.16.0-linux-x64 /usr/local/lib/nodejs
```
Set the environment variable ~/.profile

```sh
#export NODEJS_HOME=/usr/local/lib/nodejs
#export PATH=$NODEJS_HOME/bin:$PATH

if [ -d "/usr/local/lib/nodejs/bin" ] ; then
    PATH="/usr/local/lib/nodejs/bin:$PATH"
fi

```

Refresh profile:

```sh
# source ~/.profile
. ~/.profile

# Check version
node -v
npm version
```

## Installing Node.js from source code

Install the necessary build dependencies, C++ compiler, and build toolchain for your system.

[Install Python](https://github.com/mehradi-github/ref-python).


```sh
wget https://github.com/nodejs/node/archive/refs/tags/v18.16.0.tar.gz
tar -xf v18.16.0.tar.gz
cd v18.16.0
# Launch ./configure
./configure --enable-optimizations

# Launch make
make -j 8

#Test your compiled version 
make test

#Install it 
sudo make install


# Check version
node -v
npm version
```