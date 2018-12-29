## 默认安装中文语言包方案
1. 下载oss中的中文语言包（包含admin,catalog,install三个包）
2. 修改intall中的opencart.sql文件，插入语言表的第二行
~~~
INSERT INTO `oc_language` (`language_id`, `name`, `code`, `locale`, `image`, `directory`, `sort_order`, `status`) VALUES
(1, 'English', 'en-gb', 'en-US,en_US.UTF-8,en_US,en-gb,english', 'gb.png', 'english', 1, 1),
(2, ' 简体中文', 'zh-cn', 'zh_CN.UTF-8,zh_CN,zh-cn,china', 'cn.png', 'zh-CN', 1, 1);
~~~
