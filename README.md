# maix_ii_dock_display
Maix II Dock Linux ARM Develop board C code for displaying

Cross Compiling only on Linux (Debian/Ubuntu)
Prepare:
1. git clone https://github.com/sipeed/libmaix --recursive
2. download cross compiling toolchain: https://github.com/sipeed/libmaix/releases/
3. cmake > v3.9


Display size:
240x240




Build Steps:

python3 project.py distclean
export PATH=/opt/cmake-3.23.0-rc3-linux-x86_64/bin:$PATH
python3 project.py --toolchain /opt/toolchain-sunxi-musl/toolchain/bin --toolchain-prefix arm-openwrt-linux-muslgnueabi- config
python3 project.py menuconfig
python3 project.py build
python3 project.py upload
python3 project.py clean
python3 project.py distclean
