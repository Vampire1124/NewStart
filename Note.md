### 第一种：从 GitHub 上 clone 下来项目进行修改，再提交 

1. git bash 和 cmd 一样，建议使用 git bash

2. git clone 到本地指定文件夹

   - git clone git@github.com:Vampire1124/NewStart.git F:/UnityNewProject/GitHubProject

3. git clone  git@github.com:Vampire1124/NewStart.git  查看 clone 到的文件夹

   - git bash 中输入 ls
   - 输入 cd NewStart/
   - 输入 pwd 即可查看项目所在文件夹

4. 项目 clone 到指定文件夹，如何通过 Git Bash 进行上传？

   - 打开 Git Bash，cd 到你仓库文件夹，我的就是  F:/UnityNewProject/GitHubProject
   - 到达这个目录的时候后面自动有个小括号 （master） 提示这是个主分支
   - (一般不会在 master 上直接操作，而是建立分支  git branch :查看所有分支   git branch a ：创建新分支  git checkout a :切换到 a 分支上【git chekout -b a: 直接先创建再切换】，在 a 分支上修改完代码， git chekout master 切换到 master 上，git merge a ，将  a 分支合并到 master 上，合并完成 git branch -d a 删除分支 a,git tag v1.0 添加标签，也是 git checkout v1.0 切换到对应版本代码)
   - git status 即可查看提交状况
   - 之后执行 git add Note.md  将没有跟踪的文件添加进去
   - 再执行 git commit -m 'first commit' 进行提交  后面是每次提交的信息
   - git log 查看产生的所有 commmit 记录
   - git push origin master  推送到远程仓库

5. 提交的时候 Warning 警示：Permanently added the RSA host key for IP address '192.30.252.128' to the list of known host。为这个地址持久添加到 hosts 文件中。可以不用管

6. 修改文件或新建文件如何上传操作？

   - git status 查看，有红色 modified: 提示
   - 每次文件不论是原来有的还是原来没有的，修改或新添加文件，都先 git add 将修改过的或者添加的文件加进来
   - 再 git commit -m 进行上传

   7. git log 提示让你 press return  按下 q 即可退出

   ### 第二种：本地有项目NewStart2，需要在 GitHub 上建一个 NewStart2项目，然后把本地的项目中所有代码 commit 记录提交到 GitHub 上对应的项目中

   1. 本地 init 初始化一个库
      - 在本地选个地方建个文件夹  F：/GitHub
      - 打开 Git Bash，或切换到这个文件夹，cd 切换到 GitHub 文件夹
      - git status 查看这个文件夹还不是一个仓库
      - git init   执行完这个文件夹就是一个仓库
      - 在 GitHub 文件夹中创建文件 Test2.md
      - git add Test2.md
      - git commit -m 'first commit' 进行提交
      - 
   2. GitHub 上新建一个 NewStart2 项目
   3. git remote add origin git@github.com:Vampire1124/NewStart2.git
      - 给本地的项目添加一个远程仓库，origin 是给这个远程仓库起的名字，名字可以随便起。大家公认只有一个远程仓库名字就是 origin。
   4. git remote -v 查看当前项目有哪些远程仓库
   5. git push origin master 向对应的远程仓库提交代码，而这个代码是在 master 分支上。也可以提交到指定分支。
      - 此处报错。操作是，在 github 上创建项目，然后本地 git init ,没有 git pull -f -all ,就 add ,commit ,push ,导致 github 上的 readme 文件和本地版本冲突。
      - 解决办法：git push  -u origin master -f
      - 一般我们在 push 之前，都先 pull ,这样不容易导致冲突


