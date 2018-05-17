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
# 提交文件到远程版本库
```
