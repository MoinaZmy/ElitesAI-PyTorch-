1.Git 基础
1.1版本管理
1.1.1 什么是版本管理
版本管理就是一种记录文件变化的方式，以便将来查阅特定版本的文档内容。
1.1.2 人工维护文档版本存在的问题
1.文档数量多且命名不清晰导致文档版本混乱。
2.每次编辑文档需要复制，不方便。
3.多人同时编辑同一个文档，容易产生覆盖。
1.2 Git 是什么
Git是一个版本管理控制系统（缩写VCS）,它可以在任何时间点，将文档的状态作为更新记录保存起来，也可以在任何时间点，将更新记录恢复回来。
1.3 Git 的下载和安装
1.3.1 安装包下载地址：https://git-scm.com/downloads
GitHub 的页面上下载 exe 安装文件并运行
1.3.2 默认安装
1.3.3 Git 教程 https://www.runoob.com/git/git-tutorial.html
1.3.4 右击，打开Git Bash Here 打开Git
1.3.4.1 查看Git 安装版本
git --version
1.4 Git 基本的工作流程
（1）git 仓库：存放项目状态的文件夹
（2）工作目录：被Git管理的项目目录
（3）暂存区：临时存放被修改的文件
Git 仓库<-- 暂存区 <--工作目录
开发者每一次向git仓库中提交开发状态的文件，需要从工作目录中提取被修改的文件到暂存区,然后将暂存区中的文件提交到git仓库。
1.5 Git的使用
1.5.1 Git使用前的配置
在使用git前，需要告诉git你是谁，在向git仓库中提交时需要用到：
(1)配置提交人的姓名：git config --global user.name 提交人的姓名
(2)配置提交人的邮箱：git config --global user.email 提交人的邮箱
注释：
1.git config --system 对系统所有登录的用户有效
2.git config --local 只对某个仓库有效
3.git config --global 对当前用户所有的仓库有效
(3)查看git config --list
1.git config --list --global
2.git config --list --system
3.git config --list --local
注释：
（1）git config --system 对系统所有登录的用户有效
（2）git config --local 只对某个仓库有效
（3）git config --global 对当前用户所有的仓库有效
如果配置错误，重复上述操作。
或者在配置文件.gitconfig中更改:
1.5.2 提交步骤
1. git init 初始化git仓库
2. git status 查看项目文件下面的文件状态
3. git add 文件列表 添加文件到暂存区
4. git commit -m 提交信息 向git仓库中提交代码
5. git log 查看提交记录
1.5.3 撤销
（1）用暂存区中的文件覆盖工作目录中的文件：git checkout 文件名
（2）将文件从暂存区中删除： git rm --cached 文件名
