# Ubuntu下编译redis源码DEBUG版

---
### 下载源码

```
git clone https://github.com/antirez/redis.git
cd redis
git checkout 2.8.19 2.8.19
```
### 编译DEBUG

```
make distclean
make dep
make noopt DEBUG=-g OPT=-O0
```

### 单元测试
```
make test
```

### 启动调试

```
cd src
gdb ./redis-server
```


