# Opencart

## 说明
此项目是用Ansible编写的Opencart自动安装程序.

## 适用于基础环境

These are minimum requirements needed so that OpenCart can be installed and work properly.
~~~
Web Server (Apache suggested)
PHP (at least 5.4)
Curl enabled
Database (MySQLi suggested)
~~~

本程序仅适用于Websoft9的基础环境，包括：

* LAMP
* LNMP（暂时不支持）

在php7.0,mysql5.6下测试运行正常

## 适用于的操作系统

* CentOS
* Ubuntu（暂时不支持）

## 服务器需求

* 建议最低配置1核1G

## 源码包说明
1. opencart官方安装包的源码存放路径是：opencart/upload，因此Ansible下载到服务器之后还需要将源码移动到opencart目录下面
2. 目前提供Opencart官方原版（含中文语言包）、成都光大网络版两个版本，通过修改下载链接进行区分

## 用户体验改进

### 数据库随机root密码
1. 数据库root账号的随机密码存放在txt文件中（暂未实现）
2. 

### 免数据库配置

暂未实现


### 默认安装中文语言包方案
1. 手工打包中文语言包，名称为opencart,其中包含admin,catalog,install三个包，上传到OSS
2. Ansible中设置语言变量。例如设置：language: cn 
2. Ansible程序修改intall目录下的opencart.sql文件，插入语言表的第二行简体中文项（见下）
~~~
INSERT INTO `oc_language` (`language_id`, `name`, `code`, `locale`, `image`, `directory`, `sort_order`, `status`) VALUES
(1, 'English', 'en-gb', 'en-US,en_US.UTF-8,en_US,en-gb,english', 'gb.png', 'english', 1, 1),
(2, ' 简体中文', 'zh-cn', 'zh_CN.UTF-8,zh_CN,zh-cn,china', 'cn.png', 'zh-CN', 1, 1);
~~~


## Changelog
