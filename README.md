# embedfire qt app

## 野火debian-qt5-demo资料说明

1. 本代码为Qt5代码，没特意做Qt4版本兼容。
2. 本程序编译环境为qt5.11.3以上版本的。
3. windows为mingw编译器，不支持vs编译器。
4. Qt5-demo源码介绍，本程序是基于Qt5开发的，不支持Qt4直接编译。
5. FileApp.pro为多工程目录，里面的QtUi为demo的自定义基础控件库。Skin为皮肤资源文件。这2个都是必须的，且比较重要。
6. App为demo的综合程序，即为开发板看到的App程序。
7. 其他注释的工程为单个的应用程序，可取消注释，单独编译。

## 编译使用



输入命令
```bash
qmake -v 
```

若环境变量设置正确，则会出现以下信息

```bash
embedfire@dev1:~$ qmake -v
QMake version 3.0
Using Qt version 5.6.2 in /opt/fsl-imx-x11/4.1.15-2.1.0/sysroots/cortexa7hf-neon-poky-linux-gnueabi/usr/lib
```

> 以上是验证SDK安装是否成功！！

## 下载qt源码

**clone**
```bash
git clone https://github.com/Embdefire/ebf_debian_qt_demo.git
```
## 编译

```bash
./build.sh
```

如果`build.sh`不是可执行文件，可以使用以下命令添加可执行权限

```bash
chmod +x build.sh
```

## 输出

在当前目录下会创建一个`run_dir`目录，存在`App  libqui  libskin`文件，App是可以直接在开发板上运行的！
与此同时，还会打包一个`fire-app-xxxx.tar.bz2`文件，大家可以拷贝到对应的目录下解压替换掉旧的`App`。

## 清除相关内容

```bash
make distclean
```


