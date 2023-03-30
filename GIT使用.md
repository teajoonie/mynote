# git使用

### 第一次使用时配置账户  
配置用户名:  
```
git config --global user.name <yourusername>  
```
配置邮箱:  
```
git config --global user.email <youremail>
```
以上配置好后使用--list选项查看:  
```
git config --global --list
或者
git config --list
```

***
本地生成ssh放入远程仓库
```
ssh-keygen -t rsa -C "<youremail>" 
```
***

### git status 查看文件状态  
```
git status  
或者
git diff
```
### git add 将文件加入版本缓存区  
```
git add <filename>  
```

### git commit 将文件提交到本地仓库  
```
git commit [options]  
```
>options:  
>-m: 提交时要求的自定义提交信息  

### git remote 设置、读取和远程相关的信息  
```
git remote [options]  
```
>options:  
>-v: 查看fetch和push的对应地址  

### git rm 删除文件,以及相应文件跟踪清单  
```
git rm [options] <filename>
```
>options:  
>-f:强制删除已修改并且放入暂存区的文件   
>-cached:只从暂存区移除，例如日志  

### git 的glob模式字符匹配  
```
\* 等同 *
例如/etc/\*.txt和/etc/*.txt的意思一样
```
### git mv 改文件名  
```
git 
```
### git push 推送到远程仓库
```
git push  
```
