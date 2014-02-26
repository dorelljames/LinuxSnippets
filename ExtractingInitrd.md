# View, Modify and Recreate initrd.img
---------------------------------------

# Unpacking to View and/or Modify

```bash
1.) cp /boot/initramfs-{kernel-version}.img /tmp/initrd.img # copy for this example
2.) cd /tmp
3.) mv initrd.img initrd.gz # rename to .gz format
4.) gunzip initrd.gz
4.a.) ls
    
initrd

5.) mkdir initrd-tmp
6.) cd initrd-tmp
7.) cpio -id < ../initrd

9.) ls

bin dev etc init modules proc sbin selinux sys tmp var
```

# Repacking

```bash
1.) find . | cpio --create --format='newc' > /tmp/newinitrd

2.) gzip newinitrd
2.a) ls /tmp

newinitrd.gz

3.) mv /tmp/newinitrd.gz /tmp/initrd.img
```
