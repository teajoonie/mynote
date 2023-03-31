# Chocolatey 包管理器安装  
***

## 1.简介  
* Chocolatey 是一个软件管理工具，也是一个包管理器，类似于 dpkg (Apt-Get)/RPM，但在构建时考虑到了 Windows（存在差异和限制）。Chocolatey 管理包（严格来说是 nupkg 文件），而那些包管理软件（可以是安装程序，可以是运行时二进制文件，可以是 zip 或脚本）  

## 2.安装  
***
### 先决条件:  

* Windows 7+ / Windows Server 2003+  

* PowerShell v2+（由于TLS 1.2 要求，从本网站安装的最低版本为 v3 ）  

* .NET Framework 4+（如果您没有安装 .NET 4.0，安装将尝试安装它）（由于TLS 1.2 要求，从该网站安装的最低版本为  4.5 ）  

***
1. 首先以管理员模式打开powershell 
2. 输入`Get-ExecutionPolicy`,目的是为了检查Get-ExecutionPolicy不受限制。他们建议使用Bypass绕过策略来安装东西或AllSigned提高安全性。
3. 如果输入Get-ExecutionPolicy后返回的是Restricted则运行`Set-ExecutionPolicy Bypass -Scope Process`来绕过策略
4. 绕过之后再输入`Get-ExecutionPolicy`运行，查看输出，如果输出结果为Bypass就欧克了，然后下一步
5. 输入运行下面这个,就欧克了  
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
***
更多信息访问官网<https://docs.chocolatey.org/>

