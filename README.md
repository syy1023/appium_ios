
用于记录基于appium的iOS自动化测试步骤

1，在ios下安装appium

环境准备：
1，Xcode Command Line Tools

打开终端输入 命令：xcode-select --install，回车后会弹出 GUI 安装界面，同意协议安装。


2，Homebrew

在终端输入：
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"


3，Jdk
使用java -version查看是否安装成功


4，android-sdk

访问 http://www.androiddevtools.cn/ 下载 SDK Tools (24.4.1 Mac OS X) 压缩包:

直接下载链接: https://dl.google.com/android/android-sdk_r24.4.1-macosx.zip?utm_source=androiddevtools&utm_medium=website

下载完成后，解压安装包到自定义路径,tool目录下

使用终端到该路径输入命令：android-sdk-macosx/tools/android sdk 即可打开 SDK Mannager 图形界面。

勾选前三个android SDK Tools, Android SDK Platform-tools,android SDK build tools

then,
配置 android sdk 环境变量：
同 Java 环境变量配置一样，vim ~/.bash_profile 修改文件

export ANDROID_HOME=/Users/xx/Documents/android-sdk-macosx
export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_HOME/build-tools/28.0.3



使用命令，安装nodejs
brew install node
安装完成后，使用命令 node -v 和 npm -v 查看版本，检查是否安装成功


配置 npm 淘宝源：

终端使用命令：npm config set registry https://registry.npm.taobao.org

检查是否配置成功使用命令：npm config get registry


使用如下命令全量安装appium
npm install appium -g --chromedriver_cdnurl=http://cdn.npm.taobao.org/dist/chromedriver

或者指向某一版本
npm install appium@1.7.2 -g


继续安装appium-doctor
npm install appium-doctor -g

使用如下命令安装缺少的包
brew intall Carthag








​