```
sudo apt install libtool pkg-config texinfo libusb-dev libusb-1.0-0-dev libftdi-dev autoconf automake make git libftdi* libhidapi-hidraw0 software-properties-common  apt-transport-https ca-certificates
sudo ldconfig
cd mkdir ~/
mkdir ~/openocd
git clone --recursive https://github.com/whid-injector/openocd-linux openocd
cd openocd
chmod -R 755 OpenOCD_SourceCode_CH347/
cd OpenOCD_SourceCode_CH347
sudo ./bootstrap
sudo autoreconf --force --install
./configure --prefix=/home/<HERE-YOUR-USERNAME>/opeoncd/ --disable-doxygen-html --disable-doxygen-pdf --disable-gccwarnings --disable-wextra --enable-ch347
make
cd /src
./openocd --version
cd ..
make install
```
