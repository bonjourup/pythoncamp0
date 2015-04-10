##如何在Gitbook里安装disqus插件？

【历程】
本打算在window系统给Gitbook安装disqus插件的，看了若干指南没有看懂。要安装npm，然后再安装disqus。在windows系统下，要安装npm需要先安装node.js,这个又需要一通折腾。想想算了。

于是，犹豫再三，十分不情愿地想切换到ubuntu也罢。后来还是开机时，系统自己先进入ubuntu系统。那就在ubuntu系统下试试吧。不过也不是上来就安装disqus，而是各种浏览后，看python视频无果之后，才开始安装disqus。可能对disqus的安装没有成功预期，也就没有那么多动力和积极性。

不过，奇怪的是，安装disqus花费时间很短。如果不是push时间花费时间长，应该是很快就安装成功，并且一次显示成功。相当不习惯一次就弄成功，像我这样的小白已经习惯了多次不成功跌倒再爬起来的模式。一次成功很不习惯。
有点瞎猫捉了个死耗子的感觉。

花费时间较长的是，将新修改的book.json文件推送到github，gitbook花费了较长时间。明知道我在git push环节屡次出问题时粗暴地用git push --force是可以推送成功的。但是就是不想用--force方式，多次push不成功，于是，还得退到老路上，git push --force推送，成功。不过一点也不开心。为什么每次都得force？

**留下问题：没有理解git push具体的错误提示，对git还是各种不了解。需要全面的学习一下。**

###在ubuntu环境下安装gitbook disqus插件步骤如下：

1.首先安装npm
  sudu apt-get install npm
2.在npm下安装disqus插件
 $ sudo npm install gitbook-plugin-disqus -g
或者 npm install gitbook-plugin-disqus -g
   不知道两个命令有什么区别？
3.在book.json文件中添加代码后保存：
   {
        "plugins":["disqus"],
        "pluginsConfig":{
                "disqus":{
                   "shortName":"******"
                       }
                      }
   }
4.然后git更新远程仓库即可。

Ps：根据邮件列表提示搜索相关教程综合而成。
