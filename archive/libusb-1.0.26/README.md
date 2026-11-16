# LG_libusb_Android



## 编译环境

```
Ubuntu
ubuntu-21.10-desktop-amd64.iso

NDK
android-ndk-r21e-linux-x86_64.zip

libusb
libusb-1.0.26.tar.bz2
```



## NDK 下载

较新版本

https://developer.android.google.cn/ndk/downloads

较旧版本

https://github.com/android/ndk/wiki/Unsupported-Downloads 

r21e 版本 ndkVersion "21.4.7075529"

https://dl.google.com/android/repository/android-ndk-r21e-linux-x86_64.zip



```
mkdir AndroidDev
cd AndroidDev
wget https://dl.google.com/android/repository/android-ndk-r21e-linux-x86_64.zip
unzip android-ndk-r21e-linux-x86_64.zip
```



## libusb 下载

https://libusb.info/

官网 Downloads 页面下载 Latest Source (tarball) 版本



或者直接下载解压

```
wget https://github.com/libusb/libusb/releases/download/v1.0.26/libusb-1.0.26.tar.bz2
tar -jxvf libusb-1.0.26.tar.bz2
```



## 编译

Android 官方编译说明

```
https://github.com/libusb/libusb/blob/master/android/README
```



命令

```
cd /home/louis/AndroidDev/libusb-1.0.26/android/jni
export NDK=/home/louis/AndroidDev/android-ndk-r21e
$NDK/ndk-build
```



默认编译后在 android/libs 目录下生成不同平台的 libusb1.0.so 等文件

```
/home/louis/AndroidDev/libusb-1.0.26/android/libs/armeabi-v7a
/home/louis/AndroidDev/libusb-1.0.26/android/libs/arm64-v8a
/home/louis/AndroidDev/libusb-1.0.26/android/libs/x86
/home/louis/AndroidDev/libusb-1.0.26/android/libs/x86_64
```



说明

```
//1.0.26 源码
libusb-1.0.26.tar.bz2
//编译后生成的文件
libs.7z
//编译后生成的文件里的 so 库
armeabi-v7a arm64-v8a x86 x86_64
```









