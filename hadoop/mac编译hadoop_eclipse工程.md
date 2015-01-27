# Mac编译Hadoop Eclipse工程




## 编译安装protobuf


```
cd protobuf-2.5.0
./configuration
make
```
在PATH里面加入protoc的目录

## 修改Mac Java配置

```
sudo mkdir -p /Library/Java/JavaVirtualMachines/jdk1.7.0_67.jdk/Contents/Home/Classes
sudo  ln -s  \
/Library/Java/JavaVirtualMachines/jdk1.7.0_67.jdk/Contents/Home/lib/tools.jar \
/Library/Java/JavaVirtualMachines/jdk1.7.0_67.jdk/Contents/Home/Classes/classes.jar
```

## 编译hadoop源码

```
wget http://mirrors.hust.edu.cn/apache/hadoop/common/hadoop-2.6.0/hadoop-2.6.0-src.tar.gz
tar -xzvf hadoop-2.6.0-src.tar.gz
cd hadoop-2.6.0-src
mvn eclipse:eclipse
```
