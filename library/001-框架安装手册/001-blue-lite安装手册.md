# blue-lite安装手册
>1. [一. GitLab注册、创建项目](#一. GitLab注册、创建项目 "一. GitLab注册、创建项目")
	1. [1. 注册：](#1. 注册： "1. 注册：")
	1. [2. 创建项目：](#2. 创建项目： "2. 创建项目：")
1. [二．	工具安装部署（只需安装一次）](#二．	工具安装部署（只需安装一次） "二．	工具安装部署（只需安装一次）")
	1. [1．XAMPP（Apache+MySQL+PHP+PERL）建站集成软件包：](#1．XAMPP（Apache+MySQL+PHP+PERL）建站集成软件包： "1．XAMPP（Apache+MySQL+PHP+PERL）建站集成软件包：")
	1. [2. Git](#2. Git "2. Git")
	1. [3. 客户端工具（Sourcetree、Git&#34;命令行&#34;）](#3. 客户端工具（Sourcetree、Git命令行） "3. 客户端工具（Sourcetree、Git&#34;命令行&#34;）")
1. [三．SSH秘钥生成与配置（客户端&#34;Sourcetree、Git命令行&#34;与GitLab仓库通讯协议）](#三．SSH秘钥生成与配置（客户端Sourcetree、Git命令行与GitLab仓库通讯协议） "三．SSH秘钥生成与配置（客户端&#34;Sourcetree、Git命令行&#34;与GitLab仓库通讯协议）")
	1. [1．SSH秘钥生成：](#1．SSH秘钥生成： "1．SSH秘钥生成：")
	1. [2．在GitLab上增加SSH密钥：](#2．在GitLab上增加SSH密钥： "2．在GitLab上增加SSH密钥：")
	1. [Sourcetree客户端SSH秘钥配置（*注：只有windows才需要配置*）：](#Sourcetree客户端SSH秘钥配置（*注：只有windows才需要配置*）： "Sourcetree客户端SSH秘钥配置（*注：只有windows才需要配置*）：")
1. [四．	Composer、bower（独立软件包）](#四．	Composer、bower（独立软件包） "四．	Composer、bower（独立软件包）")
	1. [Mac:](#Mac: "Mac:")
	1. [Win客户端安装：](#Win客户端安装： "Win客户端安装：")
	1. [Win命令行安装：](#Win命令行安装： "Win命令行安装：")
1. [五．	Sourcetree、Git“命令行”与GitLab仓库连结克隆项目到本地](#五．	Sourcetree、Git“命令行”与GitLab仓库连结克隆项目到本地 "五．	Sourcetree、Git“命令行”与GitLab仓库连结克隆项目到本地")
	1. [命令行：](#命令行： "命令行：")
	1. [Mac：](#Mac： "Mac：")
	1. [Win：](#Win： "Win：")
1. [六．	blue-lite、blue-dot框架安装与使用](#六．	blue-lite、blue-dot框架安装与使用 "六．	blue-lite、blue-dot框架安装与使用")
	1. [blue-lie：](#blue-lie： "blue-lie：")


## 一. GitLab注册、创建项目

### 1. 注册：
<table>
  <tr>
    <td><img src="amWiki/images/图片 50.png" style="zoom:80%" /></td>
    <td>Full name：姓名标识 例 Cailin Wang<br>Username：用户名<br>Email：邮箱<br>Email confirmation：确认邮箱</td>
  </tr>
</table>

### 2. 创建项目：

 * <img src="amWiki/images/图片 51.png" style="zoom:70%" />
 * <img src="amWiki/images/图片 52.png" style="zoom:70%" />

#### 案例：
 * 项目名称：
  * siemens-emcc2018
 * 项目描述示例：
  * 框架：blue-lite
  * 客户：西门子
  * 项目：EMCC 2018
  * 日期：2018.04.18

 * 可见等级示例：
  * 私有：需要创建者授权给可见用户
  * 内部：所有系统登录人员可见
  * 公开：所有注册人员可见

<font color="red">**\*注：目前全部设为公开项目**</font>

<img src="amWiki/images/图片 53.png" style="zoom:70%" />

## 二．	工具安装部署（只需安装一次）

### 1．XAMPP（Apache+MySQL+PHP+PERL）建站集成软件包：

> 下载地址（Mac&Win）：<https://www.apachefriends.org/zh_cn/index.html>

<img src="amWiki/images/图片 54.png" style="zoom:70%" />

### 2. Git
#### 下载地址：
> Mac：<https://git-scm.com/download/mac>

<img src="amWiki/images/图片 55.png" style="zoom:70%" />

> Win：<https://git-scm.com/download/win>

<img src="amWiki/images/图片 56.png" style="zoom:70%" />

### 3. 客户端工具（Sourcetree、Git"命令行"）
#### Mac：
##### ①	SourceTree
> 下载地址：<https://www.sourcetreeapp.com/download-archives>

#### Win：

①	 Sourcetree
> 下载地址：<https://www.sourcetreeapp.com/download-archives>
>> <font color="red">**注：因为该软件需要翻墙注册，所以操作以下步骤免注册；**</font>

Ⅰ. 打开计算机或此电脑<img src="amWiki/images/图片 57.png" style="zoom:70%" /> ，在地址栏输入 <font color="#0373e4">`%LocalAppData%\Atlassian\SourceTree\`</font> 回车；

Ⅱ.在下图2的区域新建一个 <font color="#0373e4">`accounts.json`</font> 文件，然后把下列代码拷贝到里面保存。
代码：
```json
[
  {
  "$id": "1",
  "$type": "SourceTree.Api.Host.Identity.Model.IdentityAccount, SourceTree.Api.Host.Identity",
  "Authenticate": true,
  "HostInstance": {
    "$id": "2",
    "$type": "SourceTree.Host.Atlassianaccount.AtlassianAccountInstance, SourceTree.Host.AtlassianAccount",
    "Host": {
      "$id": "3",
      "$type": "SourceTree.Host.Atlassianaccount.AtlassianAccountHost, SourceTree.Host.AtlassianAccount",
      "Id": "atlassian account"
    },
    "BaseUrl": "https://id.atlassian.com/"
  },
  "Credentials": {
    "$id": "4",
    "$type": "SourceTree.Model.BasicAuthCredentials, SourceTree.Api.Account",
    "Username": "",
    "Email": null
  },
  "IsDefault": false
  }
]

```
<img src="amWiki/images/图片 58.png" style="zoom:70%" />

## 三．SSH秘钥生成与配置（客户端"Sourcetree、Git命令行"与GitLab仓库通讯协议）
### 1．SSH秘钥生成：
#### Mac：

①	终端中输入指令 <font color="#0373e4">`cat ~/.ssh/id_rsa.pub`</font> 查询本机是否已有秘钥文件；如已有秘钥地址直接copy即可；

②	如提示 <font color="red">`No such file or directory`</font>
输入指令 <font color="#0373e4">`ssh-keygen -t rsa -C "已在GitLab注册的邮箱" -b 4096`</font> 生成秘钥，然后三个回车键；

③	输入指令 <font color="#0373e4">`pbcopy < ~/.ssh/id_rsa.pub`</font> 来copy秘钥地址备用（此秘钥需要与GitLab绑定后，客户端才能与GitLab通讯）；


#### Win：
①	电脑桌面点击右键，在弹出的菜单选择 <font color="#0373e4">`Git Bash Here`</font>；
 * <img src="amWiki/images/图片 59.png" style="zoom:70%" />


②	在弹出的命令窗口输入：<font color="#0373e4">`ssh-keygen -t rsa -C "`</font> 已在GitLab注册的邮箱" 然后 <font color="#0373e4">`回车、回车、回车`</font>；
 * <img src="amWiki/images/图片 60.png" style="zoom:70%" />

③	然后输入：<font color="#0373e4">`cat ~/.ssh/id_rsa.pub`</font> 回车；
 * <img src="amWiki/images/图片 61.png" style="zoom:70%" />

④	下图红色区域是生成的SSH密钥，选取后右键copy秘钥地址备用（此秘钥需要与GitLab绑定后，客户端才能与GitLab通讯）；
 * <img src="amWiki/images/图片 62.png" style="zoom:70%" />

### 2．在GitLab上增加SSH密钥：
①	打开GitLab（git.blue-dot.cn）登录，点击右上角用户头像 -> 设置；
 * <img src="amWiki/images/图片 63.png" style="zoom:70%" />

②	点击左侧《SSH密钥》菜单，在右侧内容区域（输入SSH密钥和标题）进行密钥增加；
 * <img src="amWiki/images/图片 64.png" style="zoom:70%" />

### Sourcetree客户端SSH秘钥配置（*注：只有windows才需要配置*）：
打开 Sourcetree 点击工具 -> 选项 -> 在弹出的窗口输入SSH密钥和选择OpenSSH；
 * <img src="amWiki/images/图片 65.png" style="zoom:70%" />

## 四．	Composer、bower（独立软件包）
### Mac:

> 下载composer.phar

```sh
php -r "readfile('https://getcomposer.org/installer');" | php
# 注：如果收到 readfile 错误提示，请使用 http 链接或者在 php.ini 中开启 php_openssl.dll
```

> 将它放到 usr/local/bin 目录中中，成为全域指令。

```sh
mv composer.phar /usr/local/bin/composer
```

### Win客户端安装：

#### ①	安装 composer
> 下载地址： https://getcomposer.org/Composer-Setup.exe

### Win命令行安装：

#### ①	设置系统的环境变量 PATH 并运行安装命令下载 composer.phar 文件
```sh
php -r "readfile('https://getcomposer.org/installer');" | php
# 注：如果收到 readfile 错误提示，请使用 http 链接或者在 php.ini 中开启 php_openssl.dll

```

#### ②	在 composer.phar 同级目录创建composer.bat 文件命令
```sh
echo @php "%~dp0composer.phar" %*>composer.bat
```

#### ③	在 composer.phar 同级目录创建composer.bat 文件命令
```sh
echo @php "%~dp0composer.phar" %*>composer.bat
```

 * <img src="amWiki/images/图片 66.png" style="zoom:70%" />

## 五．	Sourcetree、Git“命令行”与GitLab仓库连结克隆项目到本地

**注：以"blue-lite"框架举例**
> 登录`git.blue-dot.cn` 项目 -> 查看项目 -> 全部 -> "Cailin Wang/blue-lite" -> 点击进入详情页复制SSH 地址；

 * <img src="amWiki/images/图片 67.png" style="zoom:70%" />
 * <img src="amWiki/images/图片 68.png" style="zoom:70%" />
 * <img src="amWiki/images/图片 69.png" style="zoom:70%" />

### 命令行：
> 在项目目录执行

```sh
# git clone 项目地址
git clone git@git.blue-dot.cn:wangcailin/blue-lite.git
```

### Mac：
> 打开`Sourcetree` 新建 -> 从URL克隆 -> 添加"源URL"、"目录路径"、"名称"-> 克隆；

 * <img src="amWiki/images/图片 70.png" style="zoom:70%" />
 * <img src="amWiki/images/图片 71.png" style="zoom:70%" />

### Win：
> 打开`Sourcetree` 点击Clone -> 添加"源URL"、"目录路径"、"名称"-> 克隆；

 * <img src="amWiki/images/图片 72.png" style="zoom:70%" />
 * <img src="amWiki/images/图片 73.png" style="zoom:70%" />

## 六．	blue-lite、blue-dot框架安装与使用

> <font color="red">**注：blue-lite（think php框架）、blue-dot（公司现有框架）**</font>
>> 初建项目时会根据项目形式选择合适的框架来进行开发；

### blue-lie：

#### Mac：

 * 在GitLab新建项目仓库，然后通过Sourcetree或Git命令行把新建的项目克隆或拉取到本地项目目录（建议放在Xampp环境运行目录下）；
 * 根据项目形式选择适合的框架，在GitLab找到框架SSH地址克隆或拉取到本地框架目录（建议放在Xampp环境运行目录下）；
 * 把克隆或拉取到本地的框架文件全部Copy到新建的项目目录下面，进行配置安装（需要给目录管理员权限）。

<font color="red">**注：以下所有的执行命令需要在项目目录操作**</font>

##### ➀ 安装composer依赖库：
```sh
composer install
```

##### ➁ 安装bower依赖库：
```sh
bower install --config.directory=public/assets/libs
```

安装的时候如果到这一步选择1或2都可以

<img src="amWiki/images/图片 74.png" style="zoom:70%" />

##### ➂ 安装think php：
```sh
php think install
```

> 后端访问地址：http://127.0.0.1（(域名)/（项目目录）/public/admin
>> 登录用户名/密码：admin/123456

> 前端访问地址：http:// 127.0.0.1(域名)/

#### Win：

安装Composer、Bower依赖库（**\*注：以下所有的执行命令需要在项目目录操作**）
```sh
composer install
bower install --config.directory=public/assets/libs
php think install
```

> 后端访问地址：http://127.0.0.1(域名)/siemens(品牌名称)/emcc(项名称)/public/admin/

> 前端访问地址：http://127.0.0.1(域名)/siemens(品牌名称)/emcc(项目名称)/public/index/siemens(品牌名称)/emcc(项目名称)/
