##Ubuntu下git和github的使用

###本地git内容和github的连接
ssh命令连接github.com的SSH服务，登录用户名为git（所有GitHub用户共享此SSH用户名）。

**测试SSH连接情况**
ssh -T git@github.com
执行之后提示：Permission denied (publickey).

这表明GitHub账户中正确设置公钥认证。下图为GitHub的SSH公钥设置界面:

GitHub的SSH服务支持OpenSSH格式的公钥认证，可以通过Ubuntu下的ssh-keygen命令创建公钥/私钥对。

ssh-keygen -C "yourname@yourcompany.com" -f ~/.ssh/github

接下来就将~/.ssh/github.pub文件内容拷贝到剪切板。设置成功后，再用ssh命令访问GitHub，会显示一条认证成功信息并退出。在认证成功的信息中还会显示该公钥对应的用户名。

ssh -T git@github.com
执行后提示：Hi github! You've successfully authenticated, but GitHub does not provide shell access.

这样就能够通过SSH的方式，直接使用Git命令访问GitHub托管服务器了。


###如何使用Git进行版本控制：
1.从服务器下载代码，准确的说应该是从GitHub服务器复制一个版本库到本地：

mkdir git
mkdir repos
cd git/repos
git clone git@github.com:"account context"/"repos name".git

2.获取到源码之后，就可以进行开发了，代码开发完成就可以提交代码：

git add .    //往暂存区域添加已添加和修改的文件，不处理删除的文件
git status   //比较本地数据目录与暂存区域的变化
git commit -m "commit directions" //提到代码到本地数据目录，并添加提交说明

3.有可能你和其他人改的是同一个文件，那么冲突的情况是在所难免的，那么在提交之后再获取一下代码，就会提示代码冲突的文件，我们需要做的就是处理这些冲突，并再次提交：

git pull     //更新代码
根据提示修改冲突文件中的代码
git add .
git commit -m "commit directions"

4.做完以上步骤，需要做的是把本地数据目录的版本库的数据同步到GitHub服务器上去，这样其他人才能够看到修改。

git push

全文引自[linux社区--Ubuntu下Git以及Github使用](http://www.linuxidc.com/Linux/2012-06/62168p2.htm)
