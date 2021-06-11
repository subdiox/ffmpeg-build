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
