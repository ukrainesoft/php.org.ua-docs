---
navigation:
  - yaf.constants.md: « Зумовлені константи
  - yaf.appconfig.md: Конфігурація програми »
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Класичний приклад каталогу для програми**

```
- index.php
- .htaccess
+ conf
  |- application.ini //Файл настроек
- application/
  - Bootstrap.php
  + controllers
     - Index.php //Контроллер по умолчанию
  + views
     |+ index
        - index.phtml //Шаблон вывода для действия по умолчанию
  + modules
  - library
  - models
  - plugins
```

**Приклад #2 Вступ**

index.php єдина точка входу в додаток, всі запити ви повинні надсилати через нього (наприклад, за допомогою .htaccess в Apache + php\_mod)

```php
<?php
define("APPLICATION_PATH",  dirname(__FILE__));

$app  = new Yaf_Application(APPLICATION_PATH . "/conf/application.ini");
$app->bootstrap() //Выполнение методов, опрделенных в Bootstrap.php
 ->run();
?>
```

**Приклад #3 Правила перенаправлення**

```
#для apache (.htaccess)
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule .* index.php

#для nginx
server {
  listen ****;
  server_name  domain.com;
  root   document_root;
  index  index.php index.md index.htm;

  if (!-e $request_filename) {
    rewrite ^/(.*)  /index.php$1 last;
  }
}

#для lighttpd
$HTTP["host"] =~ "(www.)?domain.com$" {
  url.rewrite = (
     "^/(.+)/?$"  => "/index.php/$1",
  )
}
```

**Приклад #4 Конфігурація програми**

\[yaf\];APPLICATION\_PATH має бути визначена в index.php application.directory=APPLICATION\_PATH "/application/"

;product секция должна наследовать yaf\[product:yaf\]foo=bar

**Приклад #5 Контролер за замовчуванням**

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
   /* действие по умолчанию */
   public function indexAction() {
       $this->_view->word = "hello world";
       //или
       // $this->getView()->word = "hello world";
   }
}
?>
```

**Приклад #6 Шаблон виводу за замовчуванням**

```php
<html>
 <head>
   <title>Hello World</title>
 </head>
 <body>
   <?php echo $word;?>
 </body>
</html>
```

**Приклад #7 Запуск програми**

Висновок наведеного прикладу буде схожим на:

```
<html>
 <head>
   <title>Hello World</title>
 </head>
 <body>
   hello world
 </body>
</html>
```

> **Зауваження** :
> 
> Приклад вище можна створити за допомогою генератора коду Yaf який можна знайти тут yaf@github.
