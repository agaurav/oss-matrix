### cmd snippets from everyday ops



#### verify fstab enteries 


``` bash
sudo findmnt --verify --verbose
```


### smart log for nvme disk (needs `nvme-cli` apt-pkg)


``` bash
sudo nvme smart-log /dev/nvme0n1
```


#### fast copy one disk to another (of same type, `xfs` -> `ext4` will corrupt the second disk)
as root

``` bash
dd if=/dev/nvme5n1 bs=32m | pv -s 900G | dd of=/dev/nvme2n1p1 bs=32m
# or
cat /dev/nvme5n1 > /dev/nvme2n1p1
```
