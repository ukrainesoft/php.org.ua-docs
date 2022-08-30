Конструктор класу YafApplication

-   [« YafApplication::clearLastError](yaf-application.clearlasterror.html)
    
-   [YafApplication::destruct »](yaf-application.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [YafApplication](class.yaf-application.html)
    
-   Конструктор класу YafApplication
    

# YafApplication::construct

(Yaf >=1.0.0)

YafApplication::construct - Конструктор класу YafApplication

### Опис

public **YafApplication::construct**[mixed](language.types.declarations.html#language.types.declarations.mixed) `$config`, string `$envrion`

Екземпляр [YafApplication](class.yaf-application.html)

### Список параметрів

`config`

Шлях до конфігураційного ini-файлу або масив з налаштуваннями

Якщо це шлях до ini-файлу, то в ньому має бути розділ з ім'ям [yaf.environ](yaf.configuration.html#ini.yaf.environ), що є за промовчанням "product".

> **Зауваження**
> 
> Якщо ви використовуєте ini-файл, то для покращення продуктивності дозвольте опцію [yaf.cacheconfig](yaf.configuration.html#ini.yaf.cache-config)

Параметри конфігурації (та їх значення за промовчанням):

**Приклад #1 Приклад ini-файлу**

product;Ця опція не має значення за умовчанням і обов'язково має бути задана вами application.directory=APPLICATIONPATH

;Наступні параметри мають значення за замовчуванням, вам можна їх не чіпати application.library = APPLICATIONPATH. "/library" application.dispatcher.throwException=1 application.dispatcher.catchException=1

application.baseUri=""

;розширення php-скриптів ap.ext=php

;розширення файлів шаблонів ap.view.ext=phtml

ap.dispatcher.defaultModuel=Index ap.dispatcher.defaultController=Index ap.dispatcher.defaultAction=index

;Певні модулі ap.modules=Index

`envrion`

Який розділ буде завантажено як остаточну конфігурацію

### Значення, що повертаються

### Приклади

**Приклад #2 Приклад використання **YafApplication::construct()****

```php
<?php
defined('APPLICATION_PATH')                  // APPLICATION_PATH will be used in the ini config file
    || define('APPLICATION_PATH', __DIR__));

$application = new Yaf_Application(APPLICATION_PATH.'/conf/application.ini');
$application->bootstrap()->run();
?>
```

Результатом виконання цього прикладу буде щось подібне:

**Приклад #3 Приклад використання **YafApplication::construct()****

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
$application->bootstrap()->run();
?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [YafConfigIni](class.yaf-config-ini.html)