# This are the commands used in this video
## https://www.youtube.com/watch?v=8utpbbdj0LQ

```bash
cfdisk # select dos and create a single partition

mkfs.xfs /dev/sda1

mount /dev/sda1 /mnt

pacman -Sy tmux

tmux

pcstrap /mnt base linux

## Create another window with Ctrl + b and "

genfstab /mnt>/mnt&etc/fstab;arch-chroot /mnt bash -c 'pacman -Sy grub;grub-install /dev/sda;grub-mkconfig -o /boot/grub/grub.cfg';reboot
```
