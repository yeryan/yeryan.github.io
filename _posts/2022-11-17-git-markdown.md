---
layout: article
title: Git 与 MarkDown 的使用
mathjax: true
tags: Git 
    MarkDown
---
## Git
### Git初始配置 
&emsp;1.在git设置一下身份的名字和邮箱    
&emsp;&emsp;进入到需要提交的文件夹底下。   
```git
{
    git config --global user.name "yourname"
    git config --global user.email "your@email.com"
}
``` 

&emsp;2.手动删除.ssh文件夹（直接搜索该文件夹）下的known_hosts（通常在c盘用户文件夹下）

&emsp;3.git输入命令 
```git
{
    ssh-keygen -t rsa -C "your@email.com"（请填你设置的邮箱地址）
}
``` 
>出现：
>
>Generating public/private rsa key pair. 
>
>Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):

&emsp; &emsp;一路回车，系统会自动在.ssh文件夹下生成两个文件，id_rsa和id_rsa.pub。  
&emsp; &emsp;用记事本打开id_rsa.pub，将全部的内容复制到剪切板。 

&emsp;4.打开<https://github.com/>，登陆你的账户，进入设置     
&emsp;&emsp;进入ssh设置 -> New SSH Key -> 粘贴剪切板中的内容 -> 点击 add SSH Key 

&emsp;5.在git中输入命令 
```git
{
    ssh -T git@github.com
}
``` 
&emsp;&emsp;输入命令：yes      
&emsp;&emsp;配置成功！ 

&emsp;6.新建仓库与本地连接     
&emsp;&emsp;在GitHub上新建项目。    
&emsp;&emsp;在要上传的本地文件夹中右键GitBash。   
&emsp;&emsp;输入命令创建新项目并上传：   
```git
{
    git init 
    git branch -m main  (替换默认分支名为main) 
    git status  (查看版本状态)
    git add -a  (跟踪所有文件的改变)
    git commit -m "更新日志" 
    git remote add origin 粘贴项目的SSH地址 
    git push -u origin master/main  (上传至默认分支 master/main) 
}
``` 
### Git常用命令 

```git
{
    ssh-ketgen -t rsa -C "账号"			            生成ssh密钥
    ssh -T git@github.com			                试验配置是否成功
    git config --global user.name "用户名"		
    git config --global user.email "邮箱"		
    git init					                    将本地文件夹变为git可管理的仓库
    git add .					                    将项目添加到仓库
    git commit -m "提交日志"                        提交更新日志
    git remote add origin 粘贴地址		            与仓库进行连接
    git push -u origin master			            上传
    git pull --rebase origin master			        内容合并
    git remote add origin https://github.com/yeryan/yery.github.io.git
    git branch -m main				                更改默认分支的名称为main
    git push -u origin main
    git clone 粘贴地址				                将fork的仓库同步到本地
    git branch -m master main
    git fetch origin
    git branch -u origin/main main
    git remote set-head origin -a
    git status				                        查看版本状态
}
```

## MarkDown的使用 

&emsp; 官网：<https://markdown.com.cn/intro.html> 

        
---