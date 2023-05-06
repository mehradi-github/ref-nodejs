# Installing Node.js
Installing Node.js using Linux Command Line.

- [Installing Node.js](#installing-nodejs)
  - [Installing Node.js using Linux Binaries (x64)](#installing-nodejs-using-linux-binaries-x64)



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
. ~/.profile

# Check version
node -v
npm version
```