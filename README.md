### 简单学习了一下slim框架restful的用法。
slim比较小，懒得配.ignore直接源码上传了。免composer安装
```
git clone https://github.com/moxiaonai/simpleSlim.git
```
___
创建本地数据库
```
CREATE TABLE IF NOT EXISTS `employee` (  
  `employee_id` int(11) NOT NULL,  
  `emp_name` varchar(100) NOT NULL,  
  `emp_contact` varchar(100) NOT NULL,  
  `emp_role` varchar(100) NOT NULL  
) ENGINE=InnoDB AUTO_INCREMENT=9 DEFAULT CHARSET=utf8;  
   
   
INSERT INTO `employee` (`employee_id`, `emp_name`, `emp_contact`, `emp_role`) VALUES  
(1, 'Hardik Vyas', '94085xxxxx', 'Web Developer'),  
(3, 'Raj K Joshi', '996633XXX', 'SEO Master'),  
(4, 'Ram D Rv', '55555XXX', 'Admin');  
```
___
如果是php启动服务
`cd simpleSlim/src && php -s localhost:7777`
___

如果你使用的是`apache httpd `应用服务器，请在`simpleSlim`目录下创建 `.htaccess`， 写入
```
RewriteEngine on  
RewriteCond %{REQUEST_FILENAME} !-d  
RewriteCond %{REQUEST_FILENAME} !-f  
RewriteRule . index.php [L]  
```
修改httpd.conf,在最后位置添加
```
<VirtualHost *:80>
    DocumentRoot "D:/xampp/htdocs/slim/src/public"
    ServerName 127.0.0.1
</VirtualHost>
```
访问 http://127.0.0.1/dboper.php 就能看到效果
