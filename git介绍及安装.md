
### Git介绍及安装

在介绍Github之前，首先要介绍GIT这个工具，GIT 是一个分布式版本控制软件，GitHub它为开源项目免费提供Git存储，GIT工具提供了一系列的命令用来进行本地仓库的操作，还有一系列的用语和远程Github进行链接的指令。
首先要在linux环境下安装GIT，使用下面的命令进行安装git工具.

    $ sudo apt-get install git

成功创建本地仓库的步骤：

第一步, 先要创建一个目录,查看目录， 这个目录就是用来存放仓库的，进入目录，创建仓库，进入仓库

     mkdir html
     ls
     cd html
     mkdir mygit
     cd mygit
 
第二步, 使用git init命令, 将当前目录创建成git仓库.

        git init
  
第三步，增加文件，编辑文件.

       touch file

       vim file
  
第四步，查看当前的状态，此时还没有跟踪文件.

       git status
  
第五步，把文件加到仓库中去, 只有加到仓库中了, 才可能看一下文件的变化.

       git add file
  
第六步，现在使用查看状态的命令, 看一下是目录下文件的状态，添加成功.

       git status
  
第七步，提交，快照.

       git commit
  
第八步，第一次提交需要配置用户信息和vim编辑器.

       git config --global user.name

       git config --global user.email

       git config --global core.editor vim
  
第九步，查看提交信息.

       git log

第十步，编辑文件.

       vim file
  
第十一步，查看状态.

       git status
  
第十二步，提交.

        git commit -a
   
第十三步，查看提交信息.

        git log

经过上述的步骤就成功的在本地创建了一个GIT仓库了。
