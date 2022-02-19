# ffmpeg-build

## Ubuntu 20.04
### Install dependencies
```
sudo apt install autoconf automake build-essential cmake git-core libass-dev libfreetype6-dev libgnutls28-dev libsdl2-dev libtool libva-dev libvdpau-dev libvorbis-dev libxcb1-dev libxcb-shm0-dev meson ninja-build pkg-config texinfo wget yasm zlib1g-dev libx264-dev libx265-dev libnuma-dev libvpx-dev libfdk-aac-dev libmp3lame-dev libopus-dev
```
### Configure
```
./configure --enable-gpl --enable-nonfree --enable-gnutls --enable-libass --enable-libfdk-aac --enable-libfreetype --enable-libmp3lame --enable-libopus --enable-libvorbis --enable-libvpx --enable-libx264 --enable-libx265
```
### Build
```
make
sudo make install
```

## CentOS
### Install dependencies
```
sudo dnf install autoconf automake cmake git-core libtool meson ninja-build pkg-config texinfo wget yasm libass-devel freetype-devel gnutls-devel SDL2-devel libva-devel libvdpau-devel libvorbis-devel libxcb-devel zlib-devel numactl-devel libvpx-devel lame-devel opus-devel
```
### Build x264
```
wget https://code.videolan.org/videolan/x264/-/archive/master/x264-master.tar.gz
tar xvf x264-master.tar.gz
cd x264-master
./configure --enable-shared
make install
```
### Build x265
```
wget https://github.com/videolan/x265/archive/refs/heads/master.zip -O x265-master.zip
unzip x265-master.zip
cd x265-master
cd build/linux
./make-Makefiles.bash
make install
```
### Build fdk-aac
```
wget https://sourceforge.net/projects/opencore-amr/files/latest/download -O fdk-aac.tar.gz
tar xzf fdk-aac.tar.gz
cd fdk-aac-2.0.2
./configure
make install
```
### Configure
```
./configure --enable-gpl --enable-nonfree --enable-gnutls --enable-libass --enable-libfdk-aac --enable-libfreetype --enable-libmp3lame --enable-libopus --enable-libvorbis --enable-libvpx --enable-libx264 --enable-libx265
```
### Build
```
make
sudo make install
```
