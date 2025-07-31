## git的初始化配置
版本查看
`git -v`
**用户配置**
姓名 `git config --gloabal user.name "your name"`
邮箱 `git config --global user.email "your email"`
配置信息 `git config --global --list `
## 新建仓库
方式一：
git初始化
` git init 仓库名` 
`ls -al`查看仓库
方式二
clone仓库或项目地址
`git clone 项目地址`
## git的工作区和文件状态
工作区
操作目录，写文件的地方
暂存区
将要提交的文件暂时存储的地方
本地仓库

git的特点：不用每次修改文件都需要提交，可以先放到暂存区，在一次性提交

![[Pasted image 20240618173011.png]]
## 文件添加到git仓库 
创建文件
`echo "文件内容">文件名称`
`cat 文件名称`查看文件内容
·git add
将创建的未跟踪文件添加到暂存区中，此时文件名会由红色变为绿色
`git add .`会将所有未跟踪的文件添加到暂存区
·git commit
将暂存区的内容添加到  本地仓库中，要注意些提交的信息 
`git commit -m "提交信息"`
若不输入-m，会进入vim编辑器
i：进入编辑模式
：wq退出vim
·git log
查看提交记录
## gitreset回退版本
![[Pasted image 20240618181300.png]]
x表示该区域的内容会被清除

## git diff查看差异
 比较工作区，暂存区，版本库的差异

 ## git删除文件
`rm 文件名`删除工作区的文件，但暂存区的文件还没有删除
`git status`查看文件状态![[Pasted image 20240618212138.png]]
	此时工作区的已删除，`git ls-files`查看暂存区文件, 利用`git add 文件名`删除暂存区文件.
`利用git rm 文件名`删除文件, 能将工作区和暂存区的文件都能删除，但最后要 提交一下
 ## .gitignore
 忽略的文件，不会在本地库中显示出来
 `echo 文件名 > .gitignore`将文件添加到.gitignore当中，再用`cat .gitignore`查看忽略的文件。![[Pasted image 20240619094916.png]]
 **修改.gitignore文件**
 `vi .gitignore`在此文件中写入*.log，会自动适配.log文件，加入到.gitignore文件中

 **生效的前提**
 如果要修改.gitignore文件，添加的文件不能在版本库中，要哦从版本库中删除
 `git rm --cached 文件名`删除本地库的文件
 `echo 内容 >> 文件名`>>表示在文件的下一行写入
 ## 远程仓库
 配置ssh秘钥
 在.ssh文件下用`ssh-keygen -t rsa -b 4096`进入![[Pasted image 20240619104123.png]]
 生成秘钥
 test.pub表示公共秘钥，上面的表示私有秘钥![[Pasted image 20240619104209.png]]
 如何从github上克隆项目
 `git clone ssh地址`
 **如何从本地仓库上传文件到远程仓库**
 git pull 远程仓库内容推送给本地仓库
 git push 本地仓库推送内容到远程仓库
 
  **将本地仓库上传到远程仓库**
  将my-repo上传到github中的first_repo中![[Pasted image 20240620092426.png]]
  `git remote add origin 远程仓库地址`上传到远程仓库，一次只能操作一个远程仓库，使用第二次命令会报错，只需用`git remote rm origin`删除远程分支
  使用`git push -u origin main:master` ![[Pasted image 20240620104937.png]]
  这是上传到远程仓库的master分支下
  在远程仓库修改上传到本地仓库用`git pull`![[Pasted image 20240620105412.png]]
  
  ![[Pasted image 20240620105330.png]]
  