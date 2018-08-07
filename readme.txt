或在命令行上创建一个新的存储库
echo“#yalung_git”>> README.md 
git init 
git add README.md 
git commit -m“first commit” 
git remote add origin https://github.com/yalungfish/yalung_git.git
git push -u origin master

或从命令行推送现有存储库
git remote add origin https://github.com/yalungfish/yalung_git.git
git push -u origin master

或从另一个存储库导入代码
您可以使用Subversion，Mercurial或TFS项目中的代码初始化此存储库。

要关联一个远程库，使用命令git remote add origin https://github.com/path/repo-name.git；
也可以是这样的命令：git remote add origin git@server-name:path/repo-name.git
如：git remote add origin git@github.com:yalungfish/yalung_git
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

你也许还注意到，GitHub给出的地址不止一个，还可以用https://github.com/michaelliao/gitskills.git这样的地址。实际上，Git支持多种协议，默认的git://使用ssh，但也可以使用https等其他协议。
使用https除了速度慢以外，还有个最大的麻烦是每次推送都必须输入口令，但是在某些只开放http端口的公司内部就无法使用ssh协议而只能用https。