# How to install ZeroMQ on Raspberry Pi

The following instructions should work on your Raspbian distribution. Please report any problem. :)

## Packages

```sh
sudo apt-get install libtool pkg-config build-essential autoconf automake
```

## libsodium

ZeroMQ builds against [the Sodium library](https://github.com/jedisct1/libsodium).

```sh
wget https://github.com/jedisct1/libsodium/releases/download/1.0.3/libsodium-1.0.3.tar.gz
tar -zxvf libsodium-1.0.3.tar.gz
cd libsodium-1.0.3/
./configure
make
sudo make install
```

## ZeroMQ

```sh
wget http://download.zeromq.org/zeromq-4.1.3.tar.gz
tar -zxvf zeromq-4.1.3.tar.gz
cd zeromq-4.1.3/
./configure
make
sudo make install
sudo ldconfig
```

# Optional bindings

## Python bindings: `pyzmq`

The [pyzmq package](https://github.com/zeromq/pyzmq) requires `python-dev` to compile.

```sh
sudo apt-get install python-dev
sudo pip install pyzmq
```
