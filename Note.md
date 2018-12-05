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

