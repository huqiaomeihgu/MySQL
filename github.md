## 分支

#### Git Workflow
Git Workflow工作流定义了一个围绕项目发布的严格分支模型。虽然比功能分支工作流复杂几分，但提供了用于一个健壮的用于管理大型项目的框架。

Git Wokrflow工作流没有用超出功能分支工作流的概念和命令，而是为不同的分支分配一个很明确的角色，并定义分支之间如何和什么时候进行交互。除了使用功能分支，在做准备、维护和记录发布也使用各自的分支。当然你可以用上功能分支工作流所有的好处：Pull Requests、隔离实验性开发和更高效的协作。

本地创建的仓库默认的就是master分支，可以通过以下的命令来查看本地git仓库所属的分支：

    git branch -av
    
## github 介绍

从名字就可以看出，这个网站就是提供Git仓库托管服务的，所以，只要注册一个GitHub账号，就可以免费获得Git远程仓库。

## 添加远程仓库

如果我们现在本地有一个git仓库, 我们使用remote add 命令将它添加到远程的仓库中.

    $ git remote add origin https://github.com/wangleihd/h5class.git
    
## 同步master分支

首先可以通过下面的指令去查看本地的分支是什么

    $ git branch -av
    
如果我们本地的仓库进行开发, 交进行提交commit. 那么我们本地的仓库和远程的仓库就不能保持同步了.那么我们需要把本地的这次提交也要反映在远程的仓库上. 那么我们就需要使用push命令.

    $ git push origin master
    
如果远程的仓库进行了修改，要保证与本地的仓库进行同步，使用pull命令。

    $ git pull
    
查看本地与远程是否同步了

    $ git branch -av






