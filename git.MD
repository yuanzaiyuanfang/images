1、创建分支
     创建分支很简单：git branch <分支名>
     2、切换分支
     git checkout <分支名>
     该语句和上一个语句可以和起来用一个语句表示：git checkout -b <分支名>
     3、分支合并
     比如，如果要将开发中的分支（develop），合并到稳定分支（master），
     首先切换的master分支：git checkout master。
     然后执行合并操作：git merge develop。
     如果有冲突，会提示你，调用git status查看冲突文件。
     解决冲突，然后调用git add或git rm将解决后的文件暂存。
     所有冲突解决后，git commit 提交更改。
     4、分支衍合
     分支衍合和分支合并的差别在于，分支衍合不会保留合并的日志，不留痕迹，而 分支合并则会保留合并的日志。
     要将开发中的分支（develop），衍合到稳定分支（master）。
     首先切换的master分支：git checkout master。
     然后执行衍和操作：git rebase develop。
     如果有冲突，会提示你，调用git status查看冲突文件。
     解决冲突，然后调用git add或git rm将解决后的文件暂存。
     所有冲突解决后，git rebase --continue 提交更改。
     5、删除分支
     执行git branch -d <分支名>
     如果该分支没有合并到主分支会报错，可以用以下命令强制删除git branch -D <分支名>



把本地仓库远程仓库关联 git remote add origin 地址
拉取远程仓库 git clone 地址

创建分支：git branch name
切换分支：git checkout name
推到远程：git push origin name
拉倒本地：git fetch origin nxhd-1.2.0:nxhd-1.2.0
某次提交合并到当前分支：git cherry-pick 62ecb3 

创建tag：git tag -a 标签名称 -m "说明"
提交tag：git push origin 标签名称
