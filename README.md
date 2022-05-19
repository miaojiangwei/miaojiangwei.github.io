##1.克隆远程的仓库
>git clone  远程仓库链接地址
>
##2.将修改的文件添加到暂存区
>git add  修改的文件名
>
##3.查看当前文件的状态,有哪些被修改的文件

>git status
>
##4.将暂存区的文件提交本地库

>git commit -m "提交的备注信息"
>
##5.将本地的项目与远程的绑定一下

>git remote add origin 远程仓库的地址

##6.查看添加的仓库信息

>git remote -v
>
##7.本地仓库推送到远程仓库
>git push -u origin master

##8.查看本地仓库的分支
> git branch -a

##9.查看远程仓库的分支
> git branch -r

##10.拉取更新
>git fetch

##11.推送出现504，可输入：
>git config --global --unset http.proxy
>
>git config --global --unset https.proxy



