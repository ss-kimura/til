# Install

```
wget https://files.phpmyadmin.net/phpMyAdmin/4.8.5/phpMyAdmin-4.8.5-all-languages.zip
unzip phpmyadmin.zip
mv phpmyadmin pm
mv pm DOCUMENT_ROOT/
cd DOCUMENT_ROOT
mv config.sample.inc.php config.sample.php 
```

# Setting
```
vi config.sample.php
```

```php
$cfg['Servers'][$i]['controlhost'] = '';
$cfg['Servers'][$i]['controlport'] = '';
$cfg['Servers'][$i]['controluser'] = 'USER';
$cfg['Servers'][$i]['controlpass'] = 'PW';

$cfg['LoginCookieValidity'] = 86400;
$cfg['SendErrorReports'] = 'never';
```
