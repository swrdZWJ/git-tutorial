#Git 教程
feature-A
fix-B
feature-C
一、初始设置
1.1SSH KEY
$ ssh -keygen -t  -C "your_email@example.com"
  id_rsa文件是私有-rsa.pub是公开密匙
1.2添加公开密匙
$ cat ~/.ssh/id_rsa.pub
  ssh-rsa  your_email@example.com
查看网页ssh
添加成功之后，邮箱会收到提示“公共密匙添加完成”
1.3登陆
$  ssh -T git@github.com
二、基本操作
2.1初始化仓库
mkdir git-tutorial
cd git-tutorial
git init
2.2查看仓库状态
git status
2.3README.md文件
touch README.md
2.4箱暂存区中添加文件
git add README.md
git status
2.5将当前暂存区文件实际保存到仓库的历史记录中
git commit -m "First commit"    (First commit称作提交信息，是对提交的概述)
2.6查看日志
git log
git log 命令后加目录名只会显示该目录下的日志，若是文件名只会显示该文件相关的日志。例如 git log README.md
       如果想查看提交所带来的改动 git log -p README.md
2.7 查看更改前后的差别
$ git diff  
在执行git commit  















































