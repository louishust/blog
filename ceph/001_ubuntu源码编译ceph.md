# 编译ceph源码

---
### 下载源码
>git clone --recursive https://github.com/ceph/ceph.git

### 编译DEBUG
> shell> ./autogen.sh

> shell> CXXFLAGS="-g -pg" ./configure --without-tcmalloc

> shell> make

### 常见问题
 - g++: internal compiler error: Killed (program cc1plus)
> Code:

>sudo dd if=/dev/zero of=/swapfile bs=64M count=16

>sudo mkswap /swapfile

>sudo swapon /swapfile

>After compiling, you may wish to

>Code:

>sudo swapoff /swapfile

>sudo rm /swapfile

