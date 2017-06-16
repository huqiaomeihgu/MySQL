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
    





 
