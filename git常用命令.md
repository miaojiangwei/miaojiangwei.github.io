# 1、git安装后，第一步，设置用户名和密码
```
  git config --global user.name '用户名'

  git config --global user.email '邮箱'

  --注释： 如果不加 --global 则只对当前仓库有效
```

# 2、克隆远程的仓库
```
   git clone  远程仓库链接地址
```

# 3、拉取远程仓库到指定的分支下
```
  git clone -b "分支名称" 仓库路径
```

# 4、查看分支(包括本地的和远程上的)
```
  git branch -a    
```

# 5、查看本地的分支
```
  git branch
```
# 6、查看远程上所有的分支
```
  git branch -r
```

# 7、创建本地分支（创建完是没有提示的，可以用命令git branch查看有没有创建成功
```
  git branch test01
```
# 8、创建本地分支并切换到新建分支
```
  git branch test01
  
  git checkout [分支名称]      --切换分支，切换到指定分支
  
  git checkout master      # 切换到master 分支
  git merge test01 # 将test01分支和master 分支合并，合并后的提交点属于master
```

# 9、查看添加的仓库信息

```
   git remote -v
```

# 10、将修改的文件添加到暂存区
```
  git add  修改的文件名
```

# 11、查看当前文件的状态,有哪些被修改的文件

```
   git status
```
# 12、将暂存区的文件提交本地库

```
   git commit -m "提交的备注信息
```

# 13、添加远程仓库地址

```
   git remote add origin 远程仓库的地址
   git remote add origin https://gitlab.navinfo.com/xujun/ComputerVision.git
```

# 14、本地仓库推送到远程仓库
```
   git push <远程主机名> <本地分支名>:<远程分支名>
   git push <远程主机名> <本地分支名>   --如果本地所在分支和远程分支名称一致，那冒号后面可以省略

   git push -u origin master
```

# 15、拉取更新还未合并到远程仓库的代码到分支上
```
   git fetch
```
# 16、注意：pull 则是将远程主机的master分支最新内容拉下来后与当前本地分支直接合并 fetch+merge 。
```
   git pull <远程主机名> <远程分支名>:<本地分支名>
   
   --1. 将远程主机 origin 的 master 分支拉取过来，与本地的 test01 分支合并。
   
     git pull origin master:test01
   
   --2. 如果远程分支是与当前所在的分支合并，则冒号后面的部分可以省略。
   
     git pull origin master
```
# 17、删除本地分支
```
   git branch -d test02
```

# 18、删除远程分支
```
   git branch -r -d origin/分支名    # 先执行删除操作，-r 表示remote 远程分支的意思
   
   git push origin:分支名  # 再推送操作 到远程分支
   
   git push origin -d 分支名  # 一步到位，删完即推送 -d 表示delete
```

# 19、推送出现504，可控制台输入：
```
   git config --global --unset http.proxy
   git config --global --unset https.proxy
```

