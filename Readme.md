![123](http://images2015.cnblogs.com/blog/577880/201511/577880-20151122023641374-876573777.png)
#git&github 的相关


##1.git介绍
>这些就不写了

##2.git与svn对比
>这些也不写了

##3.git代码托管平台

1. [github](https://github.com/)
2. [gitLab](http://www.gitlab.com/)
3. [bitbucket](https://bitbucket.org/)
4. [coding](coding.net) 国内的
5. [oschina](http://git.oschina.net/) 国内的

其他平台 google 一下吧

##4.git命令使用
![](http://images2015.cnblogs.com/blog/747889/201610/747889-20161026145220500-1320304386.jpg)
###常用命令
1.git add .
2.git commit －m ""

1和2 类似于 git commit －a

3.git pull 拉取
4.git push 提交
5.git status 查状态
6.git branch dev 新建分支
7.git checkout dev 切换分支
8.git reset --hard 版本号   本地恢复到某个版本
9.git rev-parse HEAD 或 git rev-parse --short HEAD  查询当前分支版本号
10.分支合并
git checkout master
git merge --no-ff yfanDev
或git rebase featureA 重新排序
11.git checkout --orphan gh-pages 创建一个无历史的分支

eg.打一个tag：

```
➜  Wangshop git:(master) git tag 2.0.1
➜  Wangshop git:(master) git tag
2.0.1
➜  Wangshop git:(master) git push --tag
Total 0 (delta 0), reused 0 (delta 0)
To git@git.yunpro.cn:wangdian/app-ui-android.git
* [new tag]         2.0.1 -> 2.0.1
➜  Wangshop git:(master) git checkout dev
Switched to branch 'dev'
➜  Wangshop git:(dev)
```



###别名alias设置

git config --global alias.co checkout  # 别名
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch

当然以上别名不是固定的，你完全可以根据自己的习惯去定制，除此之外还可以设置组合，比如：

git config --global alias.psm 'push origin master'
git config --global alias.plm 'pull origin master'

之后经常用到的 git push origin master 和 git pull origin master 直接就用 git psm 和 git plm 代替了。

一个很吊的命令：

git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative


###git stash

>当前分支暂存。这些就不写了

###分支

![](http://images2015.cnblogs.com/blog/747889/201610/747889-20161026183005062-1944621251.jpg)


###文档终极版

<http://wiki.yunpro.cn/index.php?title=Git_%E7%9A%84%E7%94%A8%E6%B3%95>

##5.git工具
*SourceTree
*git客户端

##6.其他命令：
svn 迁移到 git
git svn clone svn://center.11bbt.com/bbtwork/project/bbt2.0/02.bbtClient/02.bbtstore/02_code/02_ios/trunk/BBTB/BBTBusiness –no-metadata –trunk=trunk BBTBusine

git push.default设置：
git config --global push.default simple

//忽略.xcuserstate 文件
git rm --cached ProjectFolder.xcodeproj/project.xcworkspace/xcuserdata/myUserName.xcuserdatad/UserInterfaceState.xcuserstate
git commit -m "Removed file that shouldn't be tracked"

##7.gitignore 使用

#github 相关

* 做静态网站 <https://pages.github.com/>
* 短链生成 <http://git.io/>
* 活跃项目 <https://github.com/explore>
* 通过关键字查找项目 awesome
* 等等
