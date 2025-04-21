# kobOS

kobOS is an arch linux based distro that is configured to my likings!

## Tools

- archiso

## How to build ISO?

1. Install archiso

```bash
sudo pacman -S archiso
```

2. Clone this repo

```bash
git clone --depth 1 https://github.com/kobewijnants/kobOS.git
```

3. Build the ISO

```bash
cd kobOS/archiso
sudo rm -rf out work
sudo mkarchiso -v .
```

The ISO will be created in the out directory.
This may take some time depending on your internet connection and computer speed.

4. Test the ISO

- Burn it to a USB drive.

```bash
sudo dd if=out/archlinux-*.iso of=/dev/sdX bs=4M status=progress && sync
```

Test using a virtual machine.

```bash
qemu-system-x86_64 -cdrom out/archlinux-*.iso -m 4096 -enable-kvm
```
