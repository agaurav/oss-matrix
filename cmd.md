### cmd snippets from everyday ops


#### verify fstab enteries 


``` bash
sudo findmnt --verify --verbose
```


### smart log for nvme disk (needs `nvme-cli` apt-pkg)


``` bash
sudo nvme smart-log /dev/nvme0n1
```
