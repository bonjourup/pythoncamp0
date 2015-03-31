## GIT的使用

###1.为什么要使用Git？
  
  * 用Git的话，就算你在飞行上火车上也可以频繁第提交更新，等到了有网络的地方再上传到远程仓库
  
  * Git会对你修改文件或目录尽察眼底。所有保存在Git数据库中的东西都用哈希值指纹字串作索引，而不是靠文件名。
  
###2.正确的版本控制系统使用原则

 **一次提交只干一件事**：完成了一个新功能，修改了一个bug，写完了一节的内容，甚至是添加了一幅图片，就执行一次提交。
    如果累积较多次修改再提交，那样版本控制系统就降格成文件备份系统了。

###3.Git的初始化和配置
**Git初始化**

    　　建立一个工作目录： mkdir  workplace

    　　进入其中：　　　　 cd workplace

    　　初始化：　　　　　 git init　

　　结果：在workplace下面有一个.git目录，这个就是git版本库(repository)

**Git的配置**

.git的三个配置文件：

　　（1）config文件，在版本库.git目录下，优先级最高

    　　访问命令： cd 版本库所在目录

    　　　　　　　 git config

　　（2）.gitconfig文件，在主目录下，优先级次高

    　　访问命令： git config --global　

　　（3）gitconfig文件，在/etc目录下，优先级最低

    　　访问命令： git config --system

可以理解为system是针对系统所有用户进行的设定，而global是针对当前用户进行的设定，而.git是当前用户版本库配置设定，可以覆盖前面两个设定~

引自[不如归去-Git学习笔记(二)](http://www.cnblogs.com/melburg/articles/2603037.html)

###4.Git工作原理（可以参考廖雪峰的博客）

