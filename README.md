# git-use

> How to use git

## Create a new repository

``` bash
Create a new repository
# 创建完成后添加README.md用于记录一些关键信息
```
## 配置ssh秘钥对

``` bash
生成秘钥对
# cd ~/.ssh
# ls
# authorized_keys2  id_dsa    known_hosts config     id_dsa.pub
查看你的公钥
# cat ~/.ssh/id_rsa.pub
配置公钥到github
# 登陆你的github帐户。点击你的头像，然后 Settings -> 左栏点击 SSH and GPG keys -> 点击 New SSH key
# 然后你复制上面的公钥内容，粘贴进“Key”文本域内。 title域，自己随便起个名字
验证key是否正常工作
# ssh -T git@github.com
# Hi xxx! You've successfully authenticated, but GitHub does not # provide shell access.
# 恭喜你，你的设置已经成功了。
```
## git clone

``` bash
git clone
# 在指定目录执行 git clone git@github.com:1992chenhongwei/vue-cli-project-start.git
# 把项目克隆到本地
```
## git remote

``` bash
与远程版本库创建关联
# git remote add origin git@github.com:1992chenhongwei/git-use.git
与远程版本库删除关联
# git remote remove origin
```
## 提交过程

``` bash
git add .
# 这个命令会把当前路径下的所有文件，添加到待上传的文件列表中。
git commit -m "注释语句"
# 将add的文件commit到仓库
git push -u origin master
# 首次提交文件到远程版本库
```
## 拉取过程

``` bash
git pull origin master
# 从远程拉取最新版本到本地，且自动合并merge
git fetch  origin master
# 从远程获取最新版本到本地，不会自动合并merge
git merge orgin/master
# 合并获取到的最新代码
```
## 创建新分支并提交

``` bash
git checkout -b 'branch1'
# 创建新的分支并切换到branch1
git push -u origin branch1
# 首次提交分支branch1
```
## 合并分支到主分支

``` bash
# 进入要合并的分支拉取最新代码（如开发分支合并到master，则进入master目录）
git pull
# 查看所有分支是否都pull下来了
git branch -a
# 使用merge合并开发分支
git merge 分支名
# 查看合并之后的状态
git status 
# 有冲突的话，通过IDE解决冲突；
# 解决冲突之后，将冲突文件提交暂存区
git add 冲突文件
# 提交merge之后的结果
git commit 
# 如果不是使用git commit -m "备注" ，那么git会自动将合并的结果作为备注，提交本地仓库；
# 本地仓库代码提交远程仓库
git push
```
