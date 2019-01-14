# Opencart

## 说明
此项目是用Ansible编写的Opencart自动安装程序.

These are minimum requirements needed so that OpenCart can be installed and work properly.
~~~
Web Server (Apache suggested)
PHP (at least 5.4)
Curl enabled
Database (MySQLi suggested)
~~~

## 适用于基础环境

本程序仅适用于Websoft9的基础环境，包括：

* LAMP
* LNMP（暂时不支持）

在php7.0,mysql5.6下测试运行正常

## 适用于的操作系统

* CentOS
* Ubuntu（暂时不支持）

## 服务器需求

* 建议最低配置1核1G

## 用户体验改进

### 免数据库配置

1. Opencart从1.32开始，已经无法通过安装步骤创建数据库，故需要提前新建数据库
2. Opencart的安装步骤是可以分步骤的，并可以点击“重新开始安装”
3. Opencart可以改进预先配置好数据库，让用户无需配置数据库，降低安装难度

### 数据库随机root密码


### 默认安装中文语言包方案
1. 下载oss中的中文语言包（包含admin,catalog,install三个包）
2. 修改intall中的opencart.sql文件，插入语言表的第二行
~~~
INSERT INTO `oc_language` (`language_id`, `name`, `code`, `locale`, `image`, `directory`, `sort_order`, `status`) VALUES
(1, 'English', 'en-gb', 'en-US,en_US.UTF-8,en_US,en-gb,english', 'gb.png', 'english', 1, 1),
(2, ' 简体中文', 'zh-cn', 'zh_CN.UTF-8,zh_CN,zh-cn,china', 'cn.png', 'zh-CN', 1, 1);
~~~
