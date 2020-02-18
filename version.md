# php-app
本项目是流行的PHP应用程序自动安装项目，适用于已经安装了Websoft9提供的LAMP或LNMP环境的用户。

## 镜像自动化说明

下面描述镜像制作过程中的注意事项和特殊要求（区别于官方默认安装）

### 源码包要求
1. 大部分源码都是海外地址，建议手工将官方下载包下载到OSS
2. 下载的源码包不进行任何处理，直接上传即可

### 组件安装
除应用程序之外的组件，都通过yum或composer在线安装

### php.ini
### 网站配置文件

### ChanZhi
1. 下载页面的地址：https://www.chanzhi.org/download/chanzhi8.0-372.html;
2. 安装要求：https://www.chanzhi.org/book/chanzhieps/5.html;
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [chazhi.yml](/roles/phpapps/tasks/chanzhi.yml) 中 ```chanzhi_download_url``` 变量对应的下载链接。
   
### CmsEasy
1. 下载页面地址：https://www.cmseasy.cn/download/
2. 安装要求：https://www.cmseasy.cn/download/
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [cmseasy.yml](/roles/phpapps/tasks/cmseasy.yml) 中 ```cmseasy_download_url``` 变量对应的下载链接。

### Codiad
1. 下载页面地址：https://github.com/Codiad/Codiad/releasess
2. 安装要求：http://codiad.com/
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [codiad.yml](/roles/phpapps/tasks/codiad.yml) 中 ```codiad_version``` 变量对应的版本号。

### Dolibarr
1. 下载页面地址：https://www.dolibarr.org/downloads
2. 安装要求：https://wiki.dolibarr.org/index.php/%E5%89%8D%E6%8F%90
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [dolibarr.yml](/roles/phpapps/tasks/dolibarr.yml) 中 ```dolibarr_version``` 变量对应的版本号。

### DreamFactory
1. 下载页面地址：https://github.com/dreamfactorysoftware/dreamfactory/releasess
2. 安装要求：http://wiki.dreamfactory.com/DreamFactory/Installation
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [dreamfactory.yml](/roles/phpapps/tasks/dreamfactory.yml) 中 ```dreamfactory_version``` 变量对应的版本号。

### DzzOffice
1. 下载页面地址：https://github.com/zyx0814/dzzoffice/releasess
2. 安装要求：http://www.dzzoffice.com/corpus/org?orgid=1
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [dzzoffice.yml](/roles/phpapps/tasks/dzzoffice.yml) 中 ```dzzoffice_version``` 变量对应的版本号。

### EmpireCMS
1. 下载页面地址：http://www.phome.net/download/
2. 安装要求：http://www.phome.net/download/
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [empirecms.yml](/roles/phpapps/tasks/empirecms.yml) 中 ```empirecms_version``` 变量对应的版本号。

### EspoCRM
1. 下载页面地址：https://www.espocrm.com/download/
2. 安装要求：https://www.espocrm.com/download/
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [espocrm.yml](/roles/phpapps/tasks/espocrm.yml) 中 ```espocrm_version``` 变量对应的版本号。

### KodCloud
1. 下载页面地址：https://kodcloud.com/download/
2. 安装要求：https://kodcloud.com/help/
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [kodcloud.yml](/roles/phpapps/tasks/kodcloud.yml) 中 ```kodcloud_version``` 变量对应的版本号。

### Laravel
1. 通过 composer 安装，无需下载源码，源码可在 GitHub 下载：https://github.com/laravel/laravel/releasess
2. 安装要求：https://laravel.com/docs/6.x
3. 如何更换安装版本：运行 ```composer update``` 命令

### MantisBT
1. 下载页面地址：https://github.com/mantisbt/mantisbt/releases
2. 安装要求：https://github.com/mantisbt/mantisbt.git
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [mantisbt.yml](/roles/phpapps/tasks/mantisbt.yml) 中 ```mantisbt_version``` 变量对应的版本号。

### Matomo
1. 下载页面地址：https://github.com/matomo-org/matomo/releases
2. 安装要求：https://github.com/matomo-org/matomo
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [matomo.yml](/roles/phpapps/tasks/matomo.yml) 中 ```matomo_version``` 变量对应的版本号。

### OneThink
1. 下载页面地址：https://github.com/liu21st/onethink/releases
2. 安装要求：https://github.com/liu21st/onethink
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [onethink.yml](/roles/phpapps/tasks/onethink.yml) 中 ```onethink_version``` 变量对应的版本号。

### Pydio
1. 下载页面地址：https://github.com/pydio/pydio-core/releases
2. 安装要求：https://github.com/pydio/pydio-core
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [pydio.yml](/roles/phpapps/tasks/pydio.yml) 中 ```pydio_version``` 变量对应的版本号。

### Ranzhi
1. 下载页面地址：https://www.ranzhi.org/dynamic/5.2.stable-142.html
2. 安装要求：https://www.ranzhi.org/book/ranzhi/ranzhiinstall-5.html
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [ranzhi.yml](/roles/phpapps/tasks/ranzhi.yml) 中 ```ranzhi_download_url``` 变量对应的下载链接。

### ResourceSpace
1. 下载页面地址：https://www.resourcespace.com/download
2. 安装要求：https://www.resourcespace.com/knowledge-base/systemadmin/general_requirements
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [resourcespace.yml](/roles/phpapps/tasks/resourcespace.yml) 中 ```resourcespace_version``` 变量对应的版本号。

### SuiteCRM
1. 下载页面地址：http://suitecrm.com/download
2. 安装要求：https://docs.suitecrm.com/admin/installation-guide/downloading-installing/
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [suitecrm.yml](/roles/phpapps/tasks/suitecrm.yml) 中 ```suitecrm_version``` 变量对应的版本号。

### Symfony
1. 通过 composer 安装，无需下载源码，下载页面地址：https://github.com/symfony/symfony/releases
2. 安装要求：https://symfony.com/doc/current/reference/requirements.html
3. 如何更换安装版本：运行 ```composer update``` 命令

### TestLink
1. 下载页面地址：https://github.com/TestLinkOpenSourceTRMS/testlink-code/releases
2. 安装要求：https://github.com/TestLinkOpenSourceTRMS/testlink-code#3-system-requirements---server
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [testlink.yml](/roles/phpapps/tasks/testlink.yml) 中 ```testlink_version``` 变量对应的版本号。

### ThinkCMF
1. 下载页面地址：https://github.com/thinkcmf/portal.git
2. 安装要求：https://github.com/thinkcmf/portal
3. 如何更换安装版本：Github 目前只有一个版本。

### ThinkPHP
1. 通过 composer 安装，无需下载源码，源码下载页面地址：https://github.com/top-think/think/releases
2. 安装要求：https://www.kancloud.cn/manual/thinkphp6_0/1037481
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [thinkphp.yml](/roles/phpapps/tasks/thinkphp.yml) 中 ```thinkphp_version``` 变量对应的版本号。
4. **6.0版本**开始，必须通过Composer方式安装和更新，所以你无法通过Git下载安装。

### Vanilla
1. 下载页面地址：https://github.com/vanilla/vanilla/releases
2. 安装要求：https://docs.vanillaforums.com/developer/installation/self-hosting/#requirements
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [vanilla.yml](/roles/phpapps/tasks/vanilla.yml) 中 ```vanilla_version``` 变量对应的版本号。

### VtigerCRM
1. 下载页面地址：https://www.vtiger.com/open-source-crm/download-open-source/
2. 安装要求：https://community.vtiger.com/help/vtigercrm/administrators/installation.html
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [vtigercrm.yml](/roles/phpapps/tasks/vtigercrm.yml) 中 ```vtigercrm_download_url``` 变量对应的下载链接。

### Zurmo
1. 下载页面地址：http://zurmo.org/download
2. 安装要求：hhttp://zurmo.org/wiki/installation-requirements
3. 如何更换安装版本：在下载页面找到源码下载地址，更换 [zurmo.yml](/roles/phpapps/tasks/zurmo.yml) 中 ```zurmo_download_url``` 变量对应的版本号。

### OwnCloud
1. 上传/下载文件大小
2. 默认内置配置文件 配置好 redis
### NextCloud
1. 上传/下载文件大小(后台可设置)

2. opcache 设置
```
opcache.enable=1
opcache.enable_cli=1
opcache.interned_strings_buffer=8
opcache.max_accelerated_files=10000
opcache.memory_consumption=128
opcache.save_comments=1
opcache.revalidate_freq=1
```

3. apache vhost 需要设置 头部  Header set Referrer-Policy "no-referrer"

4. 默认内置配置文件 配置好 redis 和 默认开启SMTP的SSL/TLS
### DzzOffice
1.上传/下载文件大小

### KodCloud（可道云）
1.上传/下载文件大小

### Pydio
1.上传/下载文件大小

### ResourceSpace
1.上传/下载文件大小

### Dolibarr
1. 需修改数据库编码为 uft-8

### Drupal
1. 需将安装包下载到 oss

### EspoCRM

### Empirecms（帝国）
1. 安装路径非根目录
2. 需修改php.ini

### SuiteCRM

### VtigerCRM

### ZurmoCRM

### Ranzhi（然之协同）
### Zentao（禅道）
### chanzhiESP（蝉知）

### MantisBT

### Mediawiki
需要安装APCU
需要解决apache上传漏洞问题

### Moodle
1. 数据库配置：innodb_file_format = Barracuda...

### Opencart
1. 汉化问题：内置三个汉化包（Install,Admin,Catalog）；默认增设一个中文配置项；默认前后台为英文
2. 默认安装vQmod

### Prestashop

### Magento
1.汉化问题：内置中文包
2.部分组件需要PHP7.2,因此建议在PHP7.2的基础环境下安装
3.最低内存为756M限制，否则在线安装插件不可以使用
4.测试在线主题和插件的安装
5.V2.3技术要求：https://devdocs.magento.com/guides/v2.3/install-gde/system-requirements-tech.html

### ECSHOP

### Discuz
1.DZ3.4版本以上需PHP7.0支持
2.修改默认数据库配置文件，确保无障碍安装

### Joomla


# 企业网盘软件的通用特征
企业网盘软件镜像核心需求，如下几点需求，是用户最需要的需求

* 上传文件大小限制不能低于500M
* Office文件的在线预览、编辑
* 视频文件在线播放
* 网盘存储挂载OSS

## NextCloud 目前在国内无法安装插件


