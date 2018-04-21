# composer安装手册

## 图形界面
下载并且运行 [Composer-Setup.exe](https://getcomposer.org/Composer-Setup.exe)，它将安装最新版本的 Composer ，并设置好系统的环境变量，因此你可以在任何目录下直接使用 composer 命令。


## 命令行

### 1. 设置系统的环境变量 PATH 并运行安装命令下载 composer.phar 文件：

```php
php -r "readfile('https://getcomposer.org/installer');" | php
#（注意： 如果收到 readfile 错误提示，请使用 http 链接或者在 php.ini 中开启 php_openssl.dll）
```

### 2. 在 composer.phar 同级目录下执行命令
```sh
echo @php "%~dp0composer.phar" %*>composer.bat
```

### 3. 查看是否安装成功
```sh
composer --version
```
<img src="amWiki/images/图片 24.png" style="zoom:80%" />

### 4. 把composer.phar、composer.bat移动到php.exe目录
> （php安装目录，为了全局使用）

<img src="amWiki/images/图片 25.png" style="zoom:80%" />

<img src="amWiki/images/图片 26.png" style="zoom:80%" />
