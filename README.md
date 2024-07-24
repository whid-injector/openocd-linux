```
sudo apt install libtool pkg-config texinfo libusb-dev libusb-1.0-0-dev libftdi-dev autoconf automake make git libftdi* libhidapi-hidraw0 software-properties-common  apt-transport-https ca-certificates
sudo ldconfig
cd ~/
git clone --recursive https://github.com/whid-injector/openocd-linux temporary
cd temporary
chmod -R 755 OpenOCD_SourceCode_CH347/
cd OpenOCD_SourceCode_CH347
sudo ./bootstrap
sudo autoreconf --force --install
sudo ./configure --disable-doxygen-html --disable-doxygen-pdf --disable-gccwarnings --disable-wextra --enable-ch347
sudo make
cd /src
sudo ./openocd --version
cd ..
sudo make install
```
Now you can remove the "temporary" folder and use OpenOCD.
