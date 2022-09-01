---
navigation:
  - yaf.constants.html: « Обумовлені константи
  - yaf.appconfig.html: Конфигурация приложения »
  - index.html: PHP Manual
  - book.yaf.html: Yaf
title: Приклади
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

index.php єдина точка входу в додаток, всі запити ви повинні надсилати через нього (наприклад, за допомогою .htaccess в Apache + phpmod)

```php
<?php
define("APPLICATION_PATH",  dirname(__FILE__));

$app  = new Yaf_Application(APPLICATION_PATH . "/conf/application.ini");
$app->bootstrap() //Выполнение методов, опрделенных в Bootstrap.php
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
  index  index.php index.html index.htm;

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

yaf;APPLICATIONPATH має бути визначена в index.php application.directory=APPLICATIONPATH "/application/"

;product секція повинна успадковувати yafproduct:yaffoo=bar

**Приклад #5 Контролер за замовчуванням**

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
   /* действие по умолчанию */
   public function indexAction() {
       $this->_view->word = "hello world";
       //или
       // $this->getView()->word = "hello world";
   }
}
?>
```

**Приклад #6 Шаблон виводу за замовчуванням**

```php
<html>
 <head>
   <title>Hello World</title>
 </head>
 <body>
   <?php echo $word;?>
 </body>
</html>
```

**Приклад #7 Запуск програми**

Результатом виконання цього прикладу буде щось подібне:

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

> **Зауваження**
> 
> Приклад вище можна створити за допомогою генератора коду Yaf який можна знайти тут yaf@github.
