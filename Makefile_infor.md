
### 下面是Markfile文件中的内容

```c
CC=gcc
AFLAGS=-Wall -g
LDFLAGS= -lmysqlclient
OBJS= add.cgi del.cgi mod.cgi sel.cgi selscore.cgi mod2.cgi add2.cgi sel2.cgi sel3.cgi del2.cgi mod3.cgi del3.cgi

all:$(OBJS)

$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)

.PHONY:clean
clean:
	rm ./*.cgi
install:
		cp *.cgi /usr/lib/cgi-bin/sx/
		cp head.html footer.html /usr/lib/cgi-bin/sx/
		sudo cp -r public/ index.html index2.html login.html /var/www/html/
```

1. 下面的代码表示执行make指令的时候会编译下面制定的文件，所以如果有增加的文件需要被编译的话，就要将其放入此处。

```c
$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)
  
OBJS= add.cgi del.cgi mod.cgi sel.cgi selscore.cgi mod2.cgi add2.cgi sel2.cgi sel3.cgi del2.cgi mod3.cgi del3.cgi
```

2. 下面的代码表示执行make clean指令的时候实际上会作的动作，就是删除当前目录下的.cgi文件。

```c
clean:
	rm ./*.cgi
```

3. 下面的代码表示执行make install指令的时候实际上会作的动作。将指定的文件放在指定的路径下。如果在网页运行出错的时候，可以根据这里的存放文件的路径去查找文件是否存在的问题。

```c
install:
		cp *.cgi /usr/lib/cgi-bin/sx/
		cp head.html footer.html /usr/lib/cgi-bin/sx/
		sudo cp -r public/ index.html index2.html login.html /var/www/html/
```

只有理解了配置文件才能正确的编译运行文件。
