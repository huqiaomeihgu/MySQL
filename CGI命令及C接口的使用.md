
## Apache介绍及安装

Apache是世界使用排名第一的Web服务器软件。它可以运行在几乎所有广泛使用的计算机平台上，由于其跨平台和安全性被广泛使用，是最流行的Web服务器端软件之一。它快速、可靠并且可通过简单的API扩充，将Perl/Python等解释器编译到服务器中。

## Apache安装

    sudo apt-get update
    sudo apt-get install tasksel
    sudo tasksel

## ATOM包的安装下载

    wget -c url
    sudo dpkg -i atom-amd64.deb
    
 ## Atom editor 开环境使用的插件
 
    atom .:进入atom的界面，搜索需要的插件进行install,安装插件之后界面更加友好方便使用

    activate-power-mode：动感插件 atl + ctrl + o :打开插件
    vim-mode：vim模式
    ex-mode：实现:w功能
    monokai：高亮显示
    atom-ternjs：JavaScript 自动补全
    autoprefixer：给 CSS 添加适当的前缀
    color-picker：选颜色
    emmet：写 HTML 的神器
    atom-beautify：美化代码，空格啊什么什么的
    autoclose-html：HTML自动补全闭标签
    file-icons: 增加许多图标,在侧边蓝文件名前面的icon,,很赞
    autocomplete-modules: 自动补全插件, 有HTML, CSS, python 等
    highlight-selected: 高亮当前所选的文字, 双击后全文这个词或变量都会变高亮.
    Open In Browser: 右键打开浏览器.
    atom-clock: 在bar显示 时间
    autocomplete-js-import: 模块导入智能提示
    autocomplete-modules: 模块智能提示【node_modules】
    
## CGI

CGI(Common Gateway Interface) 是WWW技术中最重要的技术之一，有着不可替代的重要地位。CGI是外部应用程序（CGI程序）与WEB服务器之间的接口标准，是在CGI程序和Web服务器之间传递信息的过程。CGI规范允许Web服务器执行外部程序，并将它们的输出发送给Web浏览器，CGI将Web的一组简单的静态超媒体文档变成一个完整的新的交互式媒体。

## Apache开启CGI

需要在apache中开启cgi支持.

    sudo ln -s /etc/apache2/mods-available/cgi.load /etc/apache2/mods-enabled/cgi.load

## 需要重启 apache 服务器

    service apache2 restart
    
## 改完目录的权限, 方便对目录下的文件写.

    sudo mkdir /usr/lib/cgi-bin/sx
    sudo chmod 777 /usr/lib/cgi-bin/sx
    
## Makefile文件的修改，注意install所指命令前需要的是两个Tab键

    vim Makefile

    install:
      cp *.cgi /usr/lib/cgi-bin/sx
      
 Makefile文件中实际上存储的是一系列的指令,执行make clean就是执行clean标号下的指令，清除.cgi文件，执行make install实际上就是执行复制的操作。
 
 ```c
 clean:
    rm ./*.cgi
 install:
        cp *.cgi /usr/lib/cgi-bin/sx
 ```
## 安装mysql的C语言库

    sudo apt-get update
    sudo apt-get install libmysqlclient-dev
    
## 修改stu中的文件代码

    atom . :进入atom的界面进行修改
   
#### 查看Markfile文件中的指令进行操作源码文件

    make clean :清除原来的.cgi文件
    make :编译生成.cgi文件
    make install :将.cgi文件放到指定的位置处
 
运行成功之后可以在火狐浏览器中进行查看结果，输入localhost进行测试，测试成功后进入mysql数据库进行查看。


    
    
    
