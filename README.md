# ffmpeg2mp4
ffmpeg格式转换的脚本

使用ffmpeg转换文件格式的自动化脚本，对ffmpeg命令做了简单封装，支持单个文件以及整个文件夹全部转换，输出实时进度。

该脚本配置支持大多数视频格式向mp4格式的转换。

## 配置

#### 安装node

前往[nodejs.org](https://nodejs.org)下载安装

#### 配置ffmpeg路径

```
const ffmpegPath = '/usr/local/bin/ffmpeg'; //此处换成自己的路径
```

#### 安装依赖模块

进入ffmpeg2mp4目录下，执行
```
npm install
```
## 用法

```
./ffmpeg2mp4 输入文件/目录 [输出路径]
```

转换指定文件
```
$ ./ffmpeg2mp4 ./test/1.mov 
开始转换 1.mov (1/1)...
转换成功!
全部转换结束 成功:1 失败:0
输出目录:./test
```

转换文件夹下所有视频文件
```
$ ./ffmpeg2mp4 ./test/
开始转换 1.mov (1/3)...
转换成功!
开始转换 2.mov (2/3)...
转换成功!
开始转换 3.mov (3/3)...
转换成功!
全部转换结束 成功:3 失败:0
输出目录:./test/
```