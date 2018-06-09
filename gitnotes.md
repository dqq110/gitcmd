## git在linux配置:
* 在linux上安装git：sudo apt-get install git
* 输入githup的账号: git config --global user.name 'Your Name'
* 输入githup的邮箱: git config --global user.email 'email@example.com'
* 在linux上生成一个key：ssh-keygen -t rsa -C "youremail@example.com"
* 将生成的key放到githup的settings里面   [这样就配置完成了]

## git在linux常用命令:
* git clone git@github.com:dqq110/learngit.git(项目地址)
* cd learngit(项目仓库)
* vim notes.md (创建项目文件)
* 进行二大步: git add notes.md(文件名) [git add * 表示提交所有修改过的文件]
             git commit -m'wirte to notes file'  [-m后面表示本次提交的说明]   
* git push 提交到githup上
* git pull 拉下来githup中最新的代码
* git diff 查看提交了什么
* git log 查看提交历史
* git rm filename(文件名) 删除文件
* git show 查看改变
* git branch 查看本地分支
* git branch -r 查看远程分支
* git status 查看本分支的文件情况
* git checkout -b develop 新建并切换到分支
   等同于:$ git branch develop(分支名) 创建分支
         $ git checkout develop(分支名) 切换分支
* git merge <name> 合并某分支到当前分支
* git reset --hard HEAD^ 版本回退  (HEAD表示当前版本,HEAD^表示上一版本,依次类推...)
* git reset --hard commitid 回退到commitid版本，可以使用git log 查看commitid
* git checkout -- nodes.md 让这个文件回到最近一次git commit或git add时的状态。
* git log --graph --pretty=oneline --abbrev-commit:查看漂亮的代码提交历史
* git push --set-upstream origin develop(分支名):当远程仓库githup中没有开发分支时,将本地开发的分支提交到仓库里里
* git branch -d develop:删除本地的develop分支
* git push --delete origin develop 删除远程的develop分支
* git push -d origin develop:删除远程的develop分支(这个命令在ubanto没成功过)
* git branch -D develop:强行删除develop分支
* git srash 缓存工作区内容
* git stash list 查看缓存区工作内容
* git stash pop 恢复工作区
* git rebase -i commitid 将commitid后面的所有提交合并成一个commit提交
* git push --force  强制提交
* git checkout 版本号：切换到版本号对应的代码版本
