git branch 可以查看当前项目的分支情况
git barnch -d 分支名字 删除分支
git branch 分支名字 创建分支
git checkout issue2 //切换分支
切换分支之后在原来分支修改的东西切换回来之后还是这样的，道理我都懂今天第一次看
它里面的头是当前在使用的分支
合并是要先切换到主线，git merge issue2 其实应该是不用的，不同的线也可以合并

$ git reset --hard HEAD~ 取消分支合并
## rebase合并 ##

$ git checkout issue3//切换到3
Switched to branch 'issue3'
$ git rebase master//rebase到master 
rebase的时候,修改冲突的提交不是commit命令，而不是rebase指令
$ git add myfile.txt
$ git rebase --continue
Applying: 添加pull的说明