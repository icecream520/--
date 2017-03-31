git初级 git init 然后进入，然后clone ，然后修改 然后 git add git commit -m　＂说明＂　git push 
然后还有 git log git log graph gti pull origin master 拉取最新版本 $ gitk gui下确认提交记录

$ mkdir tutorial
$ cd tutorial
$ git init
Initialized empty Git repository in /Users/eguchi/Desktop/tutorial/.git/
在tutorial目录创建一个名为myfile.txt的档案，然后提交。

连猴子都懂的Git命令
$ git add myfile.txt
$ git commit -m "first commit"
[master (root-commit) a73ae49] first commit
 1 files changed, 1 insertions(+), 0 deletions(-)
 create mode 100644 myfile.txt
目前的历史记录是这样的。

目前的历史记录
教程1 操作分支
1. 建立分支
创建名为issue1的分支。

您可以通过branch命令来创建分支。

$ git branch <branchname>
创建名为issue1的分支。

$ git branch issue1
不指定参数直接执行branch命令的话，可以显示分支列表。 前面有*的就是现在的分支。

$ git branch
  issue1
* master

教程1 操作分支
2. 切换分支
若要在新建的issue1分支进行提交，需要切换到issue1分支。

要执行checkout命令以退出分支。

$ git checkout <branch>
切换到issue1分支。

$ git checkout issue1
Switched to branch 'issue1'
目前的历史记录是这样的。

目前的历史记录

Note
在checkout命令指定 -b选项执行，可以创建分支并进行切换。

$ git checkout -b <branch>
在切换到issue1分支的状态下提交，历史记录会被记录到issue1分支。在myfile.txt添加add命令的说明后再提交。

连猴子都懂的Git命令
add 把变更录入到索引中
$ git add myfile.txt
$ git commit -m "添加add的说明"
[issue1 b2b23c4] 添加add的说明
 1 files changed, 1 insertions(+), 0 deletions(-)
目前的历史记录是这样的。

目前的历史记录
