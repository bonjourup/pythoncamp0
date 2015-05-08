##如何利用Git/Github进行协作编程


> 原则： 每个参与编程协作的人员在程序仓库的分支进行编程

####1 将github相应编程仓库克隆到本地  
如果是其他人创建的仓库，使用https网络链接，克隆成功。（而不能使用地址 git@github.com：用户名/仓库名，会提示没有接入权限）
 
	~$ git clone https://github.com/用户名/仓库名

####2 建立本地分支，并切换到分支，在分支进行修改后push到远程仓库相应分支；
   
        git branch 分支名
        git checkout 分支名
    
 或者使用一条语句实现建立本地分支并切换到分支
  
    `  git checkout -b 分支名`

然后在分支上进行修改 、增加或者修改某个文件后，gitadd、gitcommit操作后，进行gitpush，命令如下：
    
    `git push --set-upstream origin 分支名`

  *解释：该语句表示将当前分支作为上行流推送到远程仓库，并在远程仓库中建立相应分支。由本地分支推送到远程仓库相应分支。*

####3 发出pullrequest请求

检查在远程仓库中分支中出现修改，在分支中，使用pullrequest请求，建立一个新的pullrequest  

####4 merge 分支  
base选择master，compare选择分支，github比较出不同，当出现不同时，merge按钮才可以成功操作。  
 merge可以由自己操作，也可以由他人操作。
   



     