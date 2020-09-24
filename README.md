
# PHP 应用软件与网站自动化安装与部署

本项目是由 [Websoft9](https://www.websoft9.com) 研发的 **PHP应用** 自动化安装程序，开发语言是 Ansible。使用本项目，只需要用户在 Linux 上运行一条命令，即可自动化安装 phpApps，让原本复杂的安装过程变得没有任何技术门槛。  

本项目支持的一系列开源PHP应用，包括：  

[chanzhi,cmseasy,codiad,dolibarr,dreamfactory,dzzoffice,empirecms,espocrm,kodcloud,laravel,mantisbt,matomo,onethink,pydio,ranzhi,resourcespace,suitecrm,symfony,testlink,thinkcmf,thinkphp,vanilla,vtigercrm,zurmo,zdoo](/roles/phpapps/tasks)等

对于更热门的PHP应用程序，我们为之开发了单独的项目

* [WordPress](https://github.com/Websoft9/ansible-wordpress)
* [Discuz](https://github.com/Websoft9/ansible-discuz)
* [Joomla](https://github.com/Websoft9/ansible-joomla)
* [Drupal](https://github.com/Websoft9/ansible-drupal)
* [ownCloud](https://github.com/Websoft9/ansible-owncloud)
* [Nextcloud](https://github.com/Websoft9/ansible-nextcloud)
* [Prestashop](https://github.com/Websoft9/ansible-prestashop)
* [Magento](https://github.com/Websoft9/ansible-magento)
* [Opencart](https://github.com/Websoft9/ansible-opencart)
* [Moodle](https://github.com/Websoft9/ansible-moodle)
* [Mediawiki](https://github.com/Websoft9/ansible-mediawiki)
* [Zentao（禅道）](https://github.com/Websoft9/ansible-zentao)

本项目是开源项目，采用 LGPL3.0 开源协议。

## 配置要求

安装本项目，确保符合如下的条件：

| 条件       | 详情       | 备注  |
| ------------ | ------------ | ----- |
| 操作系统       | CentOS7.x       |   |
| 公有云| AWS, Azure, 阿里云, 华为云, 腾讯云 | 可选 |
| 私有云|  KVM, VMware, VirtualBox, OpenStack | 可选 |
| 服务器配置 | 最低1核1G，安装时所需的带宽不低于10M |  建议采用按量100M带宽 |

## 组件

包含的核心组件为：自选的php应用 + Apache/Nginx + MySQL + PHP

```
      1：chanzhi      2: cmseasy \n
      3: codiad       4: dolibarr \n
      5: dreamfactory 6: dzzoffice\n
      7: empirecms    8: espocrm \n
      9: kodcloud     10: laravel \n
      11: mantisbt    12: matomo \n
      13: onethink    14:pydio \n
      15: ranzhi      16: resourcespace \n
      17: suitecrm    18: symfony\n
      19: testlink    20: thinkcmf \n
      21: thinkphp    22: vanilla\n
      23: vtigercrm   24: zurmo\n\n"
```

更多请见：[参数表](https://support.websoft9.com/docs/lamp/zh/stack-components.html)

## 本项目安装 PHP 应用最新版吗？

我们会定期检查版本，并测试官方版本的可用性，以保证用户可以顺利安装最新版。  

阅读应用的[版本号管理](version.md)文档，了解更多详情。

## 安装指南

以 root 用户登录 Linux，运行下面的**一键自动化安装命令**即可启动自动化部署。若没有 root 用户，请以其他用户登录 Linux 后运行 `sudo su -` 命令提升为 root 权限，然后再运行下面的脚本。

```
wget -N https://raw.githubusercontent.com/Websoft9/ansible-linux/master/scripts/install.sh; bash install.sh -r phpapps
```

脚本后启动，就开始了自动化安装，必要时需要用户做出交互式选择，然后耐心等待直至安装成功。

**安装中的注意事项：**  

1. 操作不慎或网络发生变化，可能会导致SSH连接被中断，安装就会失败，此时请重新安装
2. 安装缓慢、停滞不前或无故中断，主要是网络不通（或网速太慢）导致的下载问题，此时请重新安装

多种原因导致无法顺利安装，请使用我们在公有云上发布的 [php应用镜像](https://apps.websoft9.com) 的部署方式

## License

[LGPL-3.0](/License.md), Additional Terms: It is not allowed to publish free or paid image based on this repository in any Cloud platform's Marketplace.

Copyright (c) 2016-present, Websoft9

## 文档

文档链接：https://support.websoft9.com/docs/lamp/installation/zh/

## FAQ

- 命令脚本部署与镜像部署有什么区别？请参考：[镜像部署-vs-脚本部署](https://support.websoft9.com/docs/faq/zh/bz-product.html#镜像部署-vs-脚本部署)
- 本项目支持在 Ansible Tower 上运行吗？支持
