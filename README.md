# gitskills
## git
# remote fetch test

以下是我在学习Git过程中使用到的一些命令，学习过程中自己得到以下感悟：使用所有的命令的前提都是要对git的原理了解一下，也不是说一下子精通并搞清楚它的实现，我觉得只有在了解原理的情况下，使用这些命令才不会出现大的问题，可能在自己的个人Git仓库搞一搞没问题，但是参与比较大型的项目、涉及到比较多的人员协作时，别给别人和自己带来麻烦，虽然可能通过其他命令可以有后悔药给你。

1、git remote 查看当前远程库  
2、git remote -v (verbose)显示对应的克隆地址

3、git remote add pb git@github.com:ITyanpeng/gitskills.git添加一个新的接远程仓库，并指定一个简称

4、git fetch pd 从远程仓库抓取数据

5、git pull 如果设置了某个分支用于跟踪某个远端仓库的分支（参见下节及第三章的内容），可以使用 git pull   
命令自动抓取数据下来，然后将远端分支自动合并到本地仓库中当前分支

6、git push -u origin master 把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。推送成功后，可以立刻在GitHub页面中看到远程库的内容已经和本地一模一样。

7、git clone git@github.com:ITyanpeng/gitskills.git先有远程仓库时，本地克隆远程仓库如果有多个人协作开发，那么每个人各自从远程克隆一份就可以了。GitHub给出的地址不止一个，还可以用https://github.com/ITyanpeng/gitskills.git这样的地址。实际上，Git支持多种协议，默认的git://使用ssh，但也可以使用https等其他协议。使用https除了速度慢以外，还有个最大的麻烦是每次推送都必须输入口令，但是在某些只开放http端口的公司内部就无法使用ssh协议而只能用https。

8、git push origin master 推送数据到远程仓库

9、git remote show [remote-name] 查看远程仓库信息

10、git remote rename pd paul 远程仓库的删除和重命名

11、git remote rm paul 碰到远端仓库服务器迁移，或者原来的克隆镜像不再使用，又或者某个参与者不再贡献代码，那么需要移除对应的远端仓库，可以运行 git remote rm 命令

12、git init 初始化目录为Git可以管理的仓库  

13、git add filename 添加文件到暂存区  

14、git commit -m "your describtion" 提交修改以及评论

15、git status 查看仓库当前状态  

16、git diff 比较差异 查看修改内容

17、git log [--pretty=oneline] 显示提交日志 命令以及注释 时间按倒叙排列

18、git reset --hard HEAD^ 回退到上一个版本，回退到倒数第二个是 HEAD^^ 第一百个是HEAD~100.  HEAD:当前版本 HEAD^ 上个版本

19、git reset --hard 36121164 回退到指定版本号 可通过 git log 查询版本号

20、git reflog 查看命令记录 版本、注释

21、git diff HEAD -- filename命令可以查看工作区和版本库里面最新版本的区别  

22、git checkout -- file丢弃工作区的修改  

23、git reset HEAD file可以把暂存区的修改撤销掉  

24、git rm filename删除文件 git commit -m "remove test.txt"提交删除 git checkout -- test.txt 撤销删除  

25、git branch命令查看当前分支  

26、git branch <name> 创建分支 git checkout <name>切换分支 git checkout -b <name>创建+切换分支 git branch -d <name>删除分支  

27、git log --graph 查看分支合并历史记录  

转载请注明出处。


