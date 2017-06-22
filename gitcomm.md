
### 通过创建一个本地的仓库来查看GIT的常用指令

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

经过上述的步骤就成功的在本地创建了一个GIT仓库了.

除了上述的指令，GIT还有一些应用，使用到的GIT可以在使用中进行查看。


### 删除文件恢复

有时候, 我们不小心把文件给删除了. 想恢复这个文件时, 需要用到下面的命令.

我现在把仓库里的README这个文件给删除了. 然后再使用ls命令查看文件, 看看这个文件是否还存在.

         $ rm README
         $ ls
         $ ls -al

文件已经被删除了, 这是我们使用linux基本命令去查看文件是不是还存在这个目录中.现在我们使用git去查看一下现在仓库是什么状态

         $ git status

发现这个文件是误删了, 我们想把它恢复回来,  如果没有将这个文件提交到仓库里, 我们可以使用下面的指令将它恢复.

         $ git checkout README

然后我们再用ls查看一下文件是否存在.

     $ ls -al

再查看git仓库是状态

     $ git status

### 版本回退

什么叫版本, 一次提交就相当于一个版本. 如果更准确的说是提交的回退. 每一次提交都会将修改的状态提交到仓库中保存着, 这些信息都保存那里呢?都保存在.git的目录下.

如果想回退到上次提交的版本, 那么需要使用git reset命令.

     $ git reset --hard commitID

注意: 使用这个命令后,再使用git log命令不会查看到所有log的相关信息, 那么我们没有办法获取到后一个提交的CommitID.

     $ git log

在这里我们需要使用git reflog命令查看后一次提交的CommitID, 如果已经有了后一次提交的CommitID, 那么我们需要使用git reset命令恢复到前面提交版本.

     $ git reflog
     
     当然如果想回到某个提交状态的时候也可以使用上述的命令找到提交的ID号。
    
### 从版本库中忽略文件

如果产生了垃圾文件，那么可以将垃圾文件放到.gitignore文件中。

     $ touch .gitignore

### 版本之间对比
   
     第一条指令比较的是第一次提交的和最新一次提交的。
     
     $ git diff 

     $ git diff commitID1 commitID2

### 什么是patch

patch实际上是保存两个文件的差异.

### git生成patch

     $ git format-patch -p1

### git 打patch

打patch实际上就是回到某个状态。

     $ git am patch-name
     
