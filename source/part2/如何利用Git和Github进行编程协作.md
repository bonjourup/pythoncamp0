##如何利用Git/Github进行协作编程


### 建立分支，在分支上进行修改

1. 将github相应编程仓库克隆到本地
   
    ` git clone https://github.com/huhu8/iDoulist`
   
    **or** 克隆github新建仓库
    
    `git clone git@github.com:huhu8/test00`
    
    本地仓库中出现相应文件夹iDoulist

2. 建立本地分支，并切换到分支
   
        git branch processtest0
        git checkout processtest0
    
    或者使用一条语句实现建立本地分支并切换到分支
  
    `  git checkout -b processtest0`

3. 然后在分支上进行修改
    
    修改某个文件后，git add、git commit后
    
    `git push --set-upstream origin 分支名`

     该语句表示将当前分支作为上行流推送到远程仓库，并在远程仓库中建立相应分支。
     由本地分支推送到远程仓库相应分支。

### 合并分支

4. 检查在远程仓库中分支中出现修改，在分支中，使用pullrequest请求   合并到master中。
 
    根据提示进行操作，branch merge测试成功。
   



     