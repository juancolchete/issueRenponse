# Can't build on Arch linux #1525
Now is not possible to build darling on Arch Linux [reference](https://github.com/darlinghq/darling/issues/1525)
## solution
The problem could be solved by downgrading ffmpeg version and some depencencies to be able to build.
```bash
sudo pacman -U https://archive.archlinux.org/packages/l/libjxl/libjxl-0.9.0-1-x86_64.pkg.tar.zst
sudo pacman -U https://archive.archlinux.org/packages/l/libplacebo/libplacebo-6.338.1-1-x86_64.pkg.tar.zst
sudo pacman -U https://archive.archlinux.org/packages/l/libavif/libavif-0.9.3-1-x86_64.pkg.tar.zst
sudo pacman -U https://archive.archlinux.org/packages/r/rav1e/rav1e-0.6.6-3-x86_64.pkg.tar.zst
sudo pacman -U https://archive.archlinux.org/packages/l/libvpx/libvpx-1.8.2-2-x86_64.pkg.tar.zst 
sudo pacman -U https://archive.archlinux.org/packages/x/x265/x265-3.5-3-x86_64.pkg.tar.zst
sudo pacman -U https://archive.archlinux.org/packages/f/ffmpeg/ffmpeg-2%3A6.1.1-7-x86_64.pkg.tar.zst
```
Then re build and install
```
make
sudo make install
```
