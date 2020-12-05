```
git branch  //查看本地全部分支
git checkout -b 新分支名 //创建本地分支
git checkout -b 本地分支名 origin/远程分支名 //从远程分支上拉取并在本地创建一条新的分支（原本不存在的）
git branch -a //查看本地及远程全部分支
git branch -r //查看远程全部分支
git fetch //本地分支与远程保持同步，再次使用`git branch -a`可看到之前未同步的全部远程分支
git push --set-upstream origin 分支名 //推送本地分支到远程仓库
```

##### 