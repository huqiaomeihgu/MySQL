
### （1）CGI介绍

CGI(Common Gateway Interface) 是WWW技术中最重要的技术之一，有着不可替代的重要地位。CGI是外部应用程序（CGI程序）与WEB服务器之间的接口标准，是在CGI程序和Web服务器之间传递信息的过程。CGI规范允许Web服务器执行外部程序，并将它们的输出发送给Web浏览器，CGI将Web的一组简单的静态超媒体文档变成一个完整的新的交互式媒体。CGI编程使用的编辑器是Atom。

### （1）Apache介绍及安装

Apache是世界使用排名第一的Web服务器软件。它可以运行在几乎所有广泛使用的计算机平台上，由于其跨平台和安全性被广泛使用，是最流行的Web服务器端软件之一。它快速、可靠并且可通过简单的API扩充，将Perl/Python等解释器编译到服务器中。

### （2）Apache安装
首先更新语言库，然后进行安装服务器。
    sudo apt-get update
    sudo apt-get install tasksel
    sudo tasksel

### （3）atom包的下载，使用下面的指令：

    wget –c url

### （4）atom的安装。使用下面的指令：

    sudo dpkg –i atom-amd64.deb

### （5）Apache开启CGI

需要在apache中开启cgi支持，使用下面的指令：

    sudo ln -s /etc/apache2/mods-available/cgi.load /etc/apache2/mods-enabled/cgi.load

### （6）需要重启 apache 服务器，使用下面的指令：

    service apache2 restart

### （7）改完目录的权限, 方便对目录下的文件写，使用下面的指令：

    sudo mkdir /usr/lib/cgi-bin/sx
    sudo chmod 777 /usr/lib/cgi-bin/sx

### （8）安装mysql的C语言库，使用下面的指令：

    sudo apt-get update
    sudo apt-get install libmysqlclient-dev

### （9）添加插件，为了使atom编辑器有更加强大的功能，可以添加各种所需要的插件，可以添加的插件如下：

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

### （10）在网上下载cgi_stu的包放在执行的目录下，然后通过atom . 指令将cgi-stu中的代码用atom编辑器打开。

### （11）修改Makefile文件的内容

    首先进入编辑的页面：
    vim Makefile

    然后添加下面的语句：
    install:
      cp *.cgi /usr/lib/cgi-bin/sx
