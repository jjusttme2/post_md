---
title: 添加域控—重复的SID
date: 2018-11-12 19:14:00
tags:
 - 部署
 - 域控
 - 问题排查
---

### 场景还原
系统环境：一台Windows 2012 Server，一台Windows XP，一台Windows XP的克隆。

### 问题描述
Windows 2012 Server域控服务器已部署完成，为了测试其可用性。 需要将两台Windows XP主机添加进新建的域中。  
其中，一台Windows XP的，添加域成功。但克隆都那台Windows XP 添加域失败。如下图：
![add_d_error.png](/images/001_add_d_error.png)

可以从提示看出: <font color="red">SID出现了问题，系统建议我们用sysprep产生新的SID。</font>

### 问题分析
#### SID是什么?
 
*A machine SID is a unique identifier generated by Windows Setup that Windows uses as the basis for the SIDs for administrator-defined local accounts and groups. After a user logs on to a system, they are represented by their account and group SIDs*

SID(Security Identifiers) 翻译过来就叫作安全标识符。它是标识用户、组和计算机帐户的唯一的号码。

#### 重复的SID引发的问题
*In a Microsoft Windows Server network, duplicate SIDs can cause problems. Issues such as WSUS incompatability, Volume Licence key activation problems as well errors in Microsoft Office products. Other non Microsoft products such as Citrix do not work correctly on environments with duplidated SID.*

如果存在两个同样SID的用户，这两个帐户将被鉴别为同一个帐户。所以，克隆的Windows XP其SID与被克隆的Windows XP是完全相同的。如果不联网，相同的SID不会有问题。如果联网呢？

域控服务器会先判断其SID是否已经被使用，避免重复添加。

所以，对于clone的Windows主机，我们需要使用工具来自动修改SID，这里使用Sysprep。

#### 产生新的SID
0, 工具为Windows自带，无需安装Sysprep。 

1，首先使用右键，以管理员身份运行。  
![run_admin_cmd.png](/images/001_run_admin_cmd.png)

2，选择使用OOBE模式，点击OK.  

![001_run_mode.png](/images/001_run_mode.png)  
![001_run_mode_en.png](/images/001_run_mode_en.png)

3，等待重启

![001_reboot_winodows.png](/images/001_reboot_winodows.png)  

4，重启完后，一路next可以了。

5，再次添加域，添加成功。

### 后记
对于克隆的系统，为了保证系统的唯一性，需要创建新的SID。  

虽然重复的SID已经是一个很老的话题了，普通用户可能完全感受不到它的存在。但少了它可能会产生不必要的应用问题。

参考链接：  
The Machine SID Duplication Myth (and Why Sysprep Matters):
[https://blogs.technet.microsoft.com/markrussinovich/2009/11/03/the-machine-sid-duplication-myth-and-why-sysprep-matters/]( https://blogs.technet.microsoft.com/markrussinovich/2009/11/03/the-machine-sid-duplication-myth-and-why-sysprep-matters/)

When and How to use Sysprep:  
[http://thesolving.com/server-room/when-and-how-to-use-sysprep/#](http://thesolving.com/server-room/when-and-how-to-use-sysprep/#)
