# Clion Windows搭建 #

## 1.1 为什么选择Clion ##
Jet brains 旗下产品，习惯使用Python的Pycharm用户大多会选择使用这种轻量级的IDE。Clion没有自带的编译器，所以需要依靠强大的MinGW，对Cpp文件进行编译。这里我教大家怎么配置clion。

我认为Clion有以下一些优点：

1. 无需使用system("pause")了，由于强大的集成功能，你甚至不用看到exe界面；
2. 自动排版代码！！！Ctrl+Alt+L，解救强迫症，再也不用为排版担忧。
3. 提词、一键修改名称等常用的功能。
4. 颜色炫酷，码农的幸福感迅速提升。

## 1.2 下载Clion##

首先我们登陆[CLion的网站](http://www.jetbrains.com/clion/)，进去后你将看到这样的界面。
![](https://github.com/Klaus271/clion/blob/master/clionhome.png?raw=true)
接着注册一个账号。注意在注册选择学生账号，然后就可以免费下载专业版的了。这里不再过多赘述，比较简单。
![](https://github.com/Klaus271/clion/blob/master/signup.png?raw=true)

## 1.3搭建环境 ##

由于Clion本身不自带编译器，所以系统要求我们下载这些的东西：

1. MINGW
2. CMake
3. GDB

而事实上，我们只需要下载MinGW即可，其它都有MinGW自带了，但是值得注意的是，这里的Cmake是阉割版本，功能不多。Cmake的功能异常强大，Cmake和OpenCV做人像处理非常厉害，有兴趣的同学可以[点击这里下载](https://cmake.org/)。

可以点击[这里下载MinGW](https://sourceforge.net/projects/mingw/files/Installer/)。
![](https://github.com/Klaus271/clion/blob/master/mingwdownload.png?raw=true)
下载里面的mingw-get-setup.exe即可。
当你成功下载后，之后就不需要什么操作了，打开。

## 配置MinGW ##
安装后，我们可以看到这个界面MinGW Installation Manager，在Basic Setup中选择我图片中的这几个就可以了。
![](https://github.com/Klaus271/clion/blob/master/mingw.png?raw=true)
然后你可以喝杯咖啡，看看数学分析，大概你做完一道证明题的时间，他就下载好了。

## 配置环境变量【可跳过】 ##

相比Linux，我最讨厌Windows的一点，就是需要自行设置环境变量。python需要大量的这些工作，但是Clion这里并不需要，但是这里我将带大家过一个非常简单的过程。

首先，右键你的此电脑，或者进入控制面板，可以看到这个界面。如果找不到控制面板，可以直接在搜索里搜索advanced system settings。
![](https://github.com/Klaus271/clion/blob/master/thiscomputer.png?raw=true)

点进去后，可以看到右下角有一个环境变量，点击。
![](https://github.com/Klaus271/clion/blob/master/advanced.png?raw=true)

接着我们选择第二个框框里面的path。
![](https://github.com/Klaus271/clion/blob/master/path.png?raw=true)
进去后看到一堆东西好可怕，但是不要紧，跟你什么关系都没有，可以看到我里面已经有很多乱七八糟的路径了，就很烦。
![](https://github.com/Klaus271/clion/blob/master/new.png?raw=true)
不过我们选择右上角的新建，然后把你安装的路径复制进去。
![](https://github.com/Klaus271/clion/blob/master/newone.png?raw=true)
然后一路点击确认！不可以点击任何一个取消！就完成了！


## 配置Clion ##
之后，我们回到Clion中，在Setting里，找到Build, Execution, Deployment 一栏你将会看到一个Tool Chains。
![](https://github.com/Klaus271/clion/blob/master/clion.png?raw=true)
这里，我们在MinGW home中填写你刚刚安装MinGW的地址，我这里就是C:\MinGW，然后下面等待下面的圈圈进行跳转，然后就好了哈哈。
![](https://github.com/Klaus271/clion/blob/master/clionsuccess.png?raw=true)

## 1.4 Clion的缺点 ##
1. 首先是MinGW的缺点，这个编译器在强制转换的过程中经常出错，比如(int)10000.00 = 9999，所以大家在使用的时候要多加注意。
2. 打开比visual studio快，但是比隔壁sublime慢很多，但是相对的，其调试的功能比sublime多很多，笔visual studio又少了一些，有利有弊吧。
3. 太小众了。

## 1.5 其它要说的 ##
Jetbrain 公司出了非常多出众的IDE，各种语言都有，大家可以下载。哟与本教程较为仓促，大家可以联系老师进一步了解如何具体安装，或者发邮件给klaus271@outlook.com，和我进行联系，谢谢！
