##Qtcreator 编译配置 QtAV ##
1. 下载QtAV([https://github.com/wang-bin/QtAV.git](https://github.com/wang-bin/QtAV.git "QtAV"))和FFmpeg([http://sourceforge.net/projects/qtav/files/depends/QtAV-depends-windows-x86%2Bx64.7z/download](http://sourceforge.net/projects/qtav/files/depends/QtAV-depends-windows-x86%2Bx64.7z/download "FFmpeg"))
2. 将QtAV-depends-windows下的include和lib拷贝到QT安装目录下的include和lib下,**注意32位还是64位**,(这种做法其实污染了原始的Qt环境,但是这样做配置比较简单).
3. 打开QtAV.pro,编译用debug和release都可以。编译完成后将debug和release目录下的sdk_install.bat执行以下(将库考到合适的位置).
4. 将QtAV-depends-windows下的bin目录拷贝到debug和release目录下的bin目录。
5. QtAV-depends-windows下的bin目录加入环境变量就可以不用4了
##VS 2015 编译配置 QtAV##
1. 下载QtAV([https://github.com/wang-bin/QtAV.git](https://github.com/wang-bin/QtAV.git "QtAV"))和FFmpeg([http://sourceforge.net/projects/qtav/files/depends/QtAV-depends-windows-x86%2Bx64.7z/download](http://sourceforge.net/projects/qtav/files/depends/QtAV-depends-windows-x86%2Bx64.7z/download "FFmpeg"))
2. 将QtAV-depends-windows下的include和lib拷贝到QT安装目录下的include和lib下,**注意32位还是64位**,(这种做法其实污染了原始的Qt环境,但是这样做配置比较简单).
3. 打开Visual Studio Tools\VS2015 开发人员命令提示,通过cd命令切换到源码所在目录,通过cd命令切换到源码所在目录,执行**qmake -r -tp vc QtAV.pro**,注意问题是我装了python，里面也有qmake.exe。解决方法是绝对路径找到Qt目录下的qmake.exe

##使用 QtAV##
1. qtcreator 打开 simpleplayer，编译时找不到lib_win_\QtAV1.dll，solution:新建lib_win_,并将QtAV debug目录下的lib拷贝过来.
2. 出现了找不到QtAV.lib和另一个相同问题，solution:将lib_win_下的QtAV1.lib改名为QtAV.lib。
3. 运行不通过，solution:将QtAV-depends-windows下的bin目录拷贝到debug和release目录下的bin目录。
4. QtAV-depends-windows下的bin目录加入环境变量就可以不用3了