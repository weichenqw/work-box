

提交前先pull，避免冲突

第一种方法：（简单易懂）

1、git add .（后面有一个点，意思是将你本地所有修改了的文件添加到暂存区）

2、git commit -m""(引号里面是你的介绍，就是你的这次的提交是什么内容，便于你以后查看，这个是将索引的当前内容与描述更改的用户和日志消息一起存储在新的提交中)

3、**git pull origin 远程分支名** 这是下拉代码，将远程最新的代码先跟你本地的代码合并一下，如果确定远程没有更新，可以不用这个，最好是每次都执行以下，完成之后打开代码查看有没有冲突，并解决，如果有冲突解决完成以后再次执行1跟2的操作

4、git push origin master（git push origin 本地分支名:refs/remotes/远程分支名） 将代码推至远程就可以了



第二种方法：

1、git stash （这是将本地代码回滚值至上一次提交的时候，就是没有你新改的代码）

2、git pull origin 远程分支名（将远程的拉下来）

3、git stash pop（将第一步回滚的代码释放出来，相等于将你修改的代码与下拉的代码合并）

然后解决冲突，你本地的代码将会是最新的代码

4、git add .

5、git commit -m ""

6、git push origin master（git push origin 本地分支名:refs/remotes/远程分支名）

这几步将代码推至了远程

最后再**git pull origin 远程分支名** 一下，确保远程的全部拉下来，有的你刚提交完有人又提交了，你再拉一下会避免比的不是最新的问题

#### 常见问题及解决;

##### 每次提交都提示输入用户名及密码

​	用户名即github邮箱，密码及github密码

​	可能是当前本地的公钥出现问题

​	``

##### Git提交时提示“Please make sure you have the correct access rights and the repository exists.”的解决方法:

1.  删除.SSH文件下的known_hosts(.SSH在C:\Users\Windows用户名目录下) 

2. ` ssh-keygen -t rsa -C "你的名字/你的邮箱" `

3. ```
   Generating public/private rsa key pair.
   Enter file in which to save the key (/c/Users/Administrator/.ssh/id_rsa):
   /c/Users/Administrator/.ssh/id_rsa already exists.
   Overwrite (y/n)? y（输入y）
   Enter passphrase (empty for no passphrase):（回车）
   Enter same passphrase again:（回车）
   将生成的id_rsa.pub打开，复制公钥到github中的密钥生成页面的key（setting->SSH and GPG keys ->New SSH key）输入框下
   ```

4.  在Git中输入ssh -T git@github.com验证与github连接是否成功时 

