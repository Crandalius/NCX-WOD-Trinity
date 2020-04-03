# NCX-WOD-Trinity
WoW - Warlords of Draenor Core based on TrinityCore 6.2.4 (fixed compilation errors)

```shell
apt-get remove libssl-dev

nano /etc/apt/sources.list
#add: "deb http://security.ubuntu.com/ubuntu bionic-security main"

apt update
apt install libssl1.0-dev
apt install libboost-all-dev
apt-get install libasio-dev

cd TrinityCore
mkdir build
cd build

cmake ../ -DOPENSSL_ROOT_DIR=/usr/local/ssl -DOPENSSL_LIBRARIES=/usr/local/ssl/lib -DCMAKE_INSTALL_PREFIX=/home/wow/server -DTOOLS=0 -DWITH_WARNINGS=1 -DBOOST_INCLUDEDIR=/usr/include/boost -DBOOST_LIBRARYDIR=/usr/include/boost

make
make install
```
