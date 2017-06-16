# Linux命令总结：

## 目录的创建、删除、复制、重命名、移动，列出目录列表，

   1.  mkdir 目录名：创建目录
   
   2.  rm -rf 目录名：删除目录(不管是否有数据)
   
   3.  cp 原目录名 新目录名 -a:复制目录
   
          例如：cp dir   dir1  -a
          
               cp dir   /home/linux/dir2  -a
               
   4.  mv 原目录名 新目录名：目录重命名移动
   
   
          例如：mv dir  dir2:重命名
         
              mv dir  /home/linux/:移动
   
   5.  ls -d 目录名：列出目录列表
   
         例如：ls -d cc:cc
        
             ls -d cc/a1:cc/a1
   
    6. find  ./dir  -name  "filename"：目录中查找文件
   
## 文件的创建、删除、复制、重命名、移动，列出文件列表，查看文件内容
 
    1. touch 文件名：创建文件
   
    2. rm 文件名：删除文件
   
    3. cp 原文件名 新文件名：复制文件
   
          例如：cp file file1
          
               cp file  /home/linux/file1
    4. mv 原文件名 新文件名 ：文件重命名移动 
   
         例如：mv file file2：重命名
         
               mv file  /home/linux/：移动
               
     5. ls -al ：列出全部的文件（包含隐藏文件）
    
       ls -al *.c:列出全部的以c为后缀上午文件
        
     6. cat  file：查看文件
     
## 路径

     1. cd .:当前路径
     
     2. cd .. :回到上层路径
     
     3. pwd:查看所在路径
     
## 系统

     1. ps ax:打开进程
     
     2. sudo xrandr -s 10:屏幕放大
     
     3. sudo apt-get install x:安装
     
     4. sudo apt-get update:更新语言
     
     
## vim 的基本使用

    i：在当前字符的左边插入
    
    I：在当前行首插入
    
    a：在当前字符的右边插入
    
    A：在当前行尾插入
    
    o：在当前行下面插入一个新行
    
    O：在当前行上面插入一个新
    
    h: 向前移动一个字符
    
    j: 向上移动一行
    
    k: 向下移动一行
    
    l: 向后移动一个字符
    
    yy: 复制当前一行
    
    dd:剪切当前一行
    
    p: 粘贴内容到游标之后
    
## vim 的使用
   
   vim 有两种模式：命令模式，编辑模式，进入vin默认进入的是命令模式。
   
   按下i或a可以进入编辑模式，按ESC键可以切换到命令模式。
   
   退出的操作：shift+q:会提示保存后再退出
            
             shift+q!:不管是否保存强制退出
             
             shift+wq:保存退出
    
    可以通过以下代码练习vim：
    
    ```c
    #include <stdio.h> 
    int main(void) {
    printf("hello \n");
    return 0;
    }
    ```





 
