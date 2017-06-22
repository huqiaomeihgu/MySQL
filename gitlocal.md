

## 步骤：

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
        
经过上述的步骤，本地GIT仓库就成功的建好了。
