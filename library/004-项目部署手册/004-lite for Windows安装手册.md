# blue-lite for Windows完全安装手册

## 1. 安装Xampp(只需安装一次)
下载地址：https://www.apachefriends.org/zh_cn/index.html

## 2. 安装git(只需安装一次)
下载地址：https://git-scm.com/download/win
```
Win7以下需要单独安装 .Net Framework 4.5 再安装 git，
下载地址：https://www.microsoft.com/zh-cn/download/details.aspx?id=30653
```

<img src="amWiki/images/图片 23.png" style="zoom:80%" />

## 3. 安装composer(只需安装一次)
在命令行执行

```sh
composer --version
```

如果没有出来版本号则跳转到[composer安装教程](?file=003-工具安装教程/001-composer安装教程 "composer安装教程")

## 4. 安装bower(只需安装一次)
在命令行执行

```sh
bower --version
```

如果没有出来版本号则跳转到[bower安装教程](?file=003-工具安装教程/002-bower安装教程 "bower安装教程")

## 5. 安装SourceTree(只需安装一次)
见[SourceTree for Windows](?file=003-工具安装教程/004-SourceTree for Windows "SourceTree for Windows")安装教程

## 6. 生成 SSH 密钥(此密钥需要分别添加到gitlab、SourceTree里面)

见[配置秘钥操作](?file=001-GitLab使用手册/002-配置秘钥操作 "配置秘钥操作")

## 7. 这部分为后端程序操作所用
在gitlab仓库获取《blue-lite》框架到本地目录，该框架获取到本地后不能当作项目进行直接操作，新建的项目需要copy整个框架文件到新建的目录，框架会根据实际情况进行不定期更新；

## 8. 在gitlab 找到并复制《blue-lite》框架SSH地址（如下三张图1-5操作步骤）
- <img src="amWiki/images/图片 36.png" style="zoom:60%" />
- <img src="amWiki/images/图片 37.png" style="zoom:60%" />
- <img src="amWiki/images/图片 38.png" style="zoom:70%" />
- 打开 SourceTree 点击 Clone -> 添加SSH与本地存储目录（这个目录建议大家放在Xampp/htdocs/品牌名称/项目名称），把框架克隆到本地，以后框架有新版本更新时只需点击“拉取”就可以获取到新版本；
- <img src="amWiki/images/图片 39.png" style="zoom:80%" />
- <img src="amWiki/images/图片 40.png" style="zoom:80%" />

## 9. 新项目操作流程

 - 在gitlab 创建新项目（如果gitlab已有所要创建的项目只需按照上一个步骤操作就好
  - <img src="amWiki/images/图片 41.png" style="zoom:50%" />
  - <img src="amWiki/images/图片 42.png" style="zoom:80%" />
 - 打开 SourceTree 点击 Clone，添加 SSH地址、本地存储目录地址（这个目录建议大家放在Xampp/htdocs/品牌名称/项目名称），点击克隆；
  - <img src="amWiki/images/图片 43.png" style="zoom:80%" />
  - <img src="amWiki/images/图片 44.png" style="zoom:80%" />
 - 然后把已经克隆好的blue-lite框架文件复制到新建的项目目录里面;
  - <img src="amWiki/images/图片 45.png" style="zoom:100%" />
  - <img src="amWiki/images/图片 46.png" style="zoom:80%" />

## 10. 在项目目录执行 composer、bower命令行操作（每个项目都需要重新执行下面的安装命令）：

```sh
  composer install
  bower install --config.directory=public/assets/libs
  php think install
```
#### 安装完成后：

 - 后端访问地址：http://127.0.0.1/siemens(品牌名称)/emcc(项名称)/public/admin/
 - 前端访问地址：http://127.0.0.1/siemens(品牌名称)/emcc(项目名称)/public/index/siemens(品牌名称)/emcc(项目名称)/
