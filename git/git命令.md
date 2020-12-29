##### git本地及远程分支管理

```
git branch  //查看本地全部分支
git checkout -b 新分支名 //创建本地分支
git checkout -b 本地分支名 origin/远程分支名 //从远程分支上拉取并在本地创建一条新的分支（原本不存在的）
git branch -a //查看本地及远程全部分支
git branch -r //查看远程全部分支
git branch -vv //查看本地分支与远程分支关联关系
git fetch //本地分支与远程保持同步，再次使用`git branch -a`可看到之前未同步的全部远程分支
git push --set-upstream origin 分支名 //推送本地分支到远程仓库
git remote show origin //追踪本地分支和仓库的关系
git remote prune origin //将仓库中已删除的分支与本地分支的追踪关系删掉
git branch -D ‘分支名’ //本地分支删除
git branch -m 旧分支名 新分支名 //建本地分支名重命名
git push origin :旧分支名 //会在`origin`仓库中匹配分支
```

常见问题：

​	1.本地分支与远程分支别名不同导致无法`pull`上去，建议别名保持一致

##### 合并后冲突

```
git merge --abort //抛弃合并状态并尝试重建合并前的状态，如果有未commit的文件，可能无法重现合并前状态
```

##### 暂存代码

```
git stash   //已修改代码存入暂存区
git stash list  //查看暂存区列表
git stash apply  //恢复暂存区代码
```

##### 本地仓库

```
git-reset //撤销上一次commit记录

```

