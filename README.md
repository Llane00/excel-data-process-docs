# excel按渠道自动切分工具

## 1. 关于安装运行环境 NodeJs

在[官网](https://nodejs.org/en/)下载安装包（推荐LTS版本）
打开安装包一路点下一步

windows 64位.msi 安装包

如：https://nodejs.org/dist/v14.15.1/node-v14.15.1-x64.msi


mac下也有对应的自动安装包

如：https://nodejs.org/dist/v14.15.1/node-v14.15.1.pkg

---

## 2.检测是否已经安装成功
windows下 win + r ，然后在输入框输入cmd回车确定打开命令提示符
，输入: 
```
node --version
```

如果是在mac下需要打开终端，
同样输入：
```
node --version
```

如果输出类似 v14.9.0 软件版本号则安装运行环境成功

---

## 3.软件工具的文件目录介绍
正常使用中只涉及到以下三个文件夹：

input_file   //excel源文件放入目录

output_file  //输出excel结果文件目录

config.js   //渠道配置文件

windows_run.bat  //windows下软件运行入口（可双击执行）

unix_run.sh  //unix下软件运行入口

---

## 4.使用工具

### 4.1 放置源文件：
在input_file文件夹下放入需要处理的源文件excel。
注意excel需要另存为.xlsx格式，并命名为1。

*正常input_file下应该只存在一个1.xlsx文件

### 4.2 运行程序：
windows系统在软件文件根目录下双击windows_run.bat即可，

mac或者其他unix系统需要在终端中输入：

```
./unix_run.sh
```

运行成功后会在output_file目录下看到本次处理切分的excel文件，
软件可以多次运行，会自动覆盖上一次的结果

### 4.3 自定义渠道筛选配置

配置文件为根目录下config.js文件

筛选纬度主要分为主渠道组，子渠道，渠道数字编号，日期范围

注意除了渠道的中文名字，其余符号都需要在英文输入法（半角）下输入，如 ":{}[] 等符号。

渠道数字编号可以是范围如：[1, 5] 表示筛选1到5的编号。
也可以是单个数字，如 6 表示只筛选单个数字编号

---

2020-12-05 v1.0
@copyright Llane00
https://github.com/Llane00/excel-data-process
