# GitHub-Use
## Git
1. （先进入项目文件夹）通过命
令 git init 把这个目录变成git可以管理的仓库
> git init

2. 把文件添加到版本库中，使用命令 git add .添加到暂存区里面去，不要忘记后面的小数点“.”，意为添加文件夹下的所有文件
> git add .

3. 用命令 git commit告诉Git，把文件提交到仓库。引号内为提交说明
> git commit -m 'first commit'

4. 关联到远程库
git remote add origin 你的远程库地址
如：
> git remote add origin https://github.com/huangjie314/GitHub-Use.git

> git remote add origin git@github.com:haungjie314/GitHub-Use.git

5. 获取远程库与本地同步合并（如果远程库不为空必须做这一步，否则后面的提交会失败）
> git pull --rebase origin master

6. 把本地库的内容推送到远程，使用 git push命令，实际上是把当前分支master推送到远程。执行此命令后会要求输入用户名、密码，验证通过后即开始上传。
> git push -u origin master

- 状态查询命令
> git status

***
* 如何取消一个目录的git初始化?
执行rm -rf .git 删掉.git文件即可
> rm -rf .git

#### git 删除分支和删除文件夹?
* 拉取远程的Repo到本地（如果已经在本地，可以略过） 
> git clone *******
* 删除分支
    - 1.1 查看所有分支
        > git branch -a

    - 1.2 删除HEAD分支
        > git push origin --delete HEAD

* 删除文件夹或者某个单一文件
  - 1.1 查看本地分支下的文件
    >ls
  - 1.2 删除文件
    > git rm **
  - 1.3 删除文件夹
    > git rm  *** -r -f
  - 1.4 同步删除操作到远程分支
    > git commit -m "delete handle"
  - 1.5 提交分支
    > git push origin master

