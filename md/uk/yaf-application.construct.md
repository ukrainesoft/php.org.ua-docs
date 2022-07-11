- [« Yaf_Application::clearLastError](yaf-application.clearlasterror.md)
- [Yaf_Application::\_\_destruct »](yaf-application.destruct.md)

- [PHP Manual](index.md)
- [Yaf_Application](class.yaf-application.md)
- Конструктор класу Yaf_Application

# Yaf_Application::\_\_construct

(Yaf \>=1.0.0)

Yaf_Application::\_\_construct - Конструктор класу Yaf_Application

### Опис

public
**Yaf_Application::\_\_construct**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$config`, string `$envrion` = ?)

Примірник [Yaf_Application](class.yaf-application.md).

### Список параметрів

`config`
Шлях до конфігураційного ini-файлу або масив із налаштуваннями

Якщо це шлях до ini-файлу, то в ньому повинен бути розділ з
ім'ям [yaf.environ](yaf.configuration.md#ini.yaf.environ), що є
за промовчанням "product".

> **Примітка**:
>
> Якщо ви використовуєте ini-файл, то для покращення продуктивності,
> дозвольте опцію
> [yaf.cache_config](yaf.configuration.md#ini.yaf.cache-config).

Параметри конфігурації (та їх значення за замовчуванням):

**Приклад #1 Приклад ini-файлу**

`` inicode
[product]
;Ця опція не має значення за умовчанням і обов'язково має бути задана вами
application.directory=APPLICATION_PATH

;Наступні параметри мають значення за замовчуванням, вам можна їх не чіпати
application.library = APPLICATION_PATH . "/library"
application.dispatcher.throwException=1
application.dispatcher.catchException=1

application.baseUri=""

;розширення php-скриптів
ap.ext=php

;розширення файлів шаблонів
ap.view.ext=phtml

ap.dispatcher.defaultModuel=Index
ap.dispatcher.defaultController=Index
ap.dispatcher.defaultAction=index

;Певні модулі
ap.modules=Index
````

`envrion`
Який розділ буде завантажено як остаточну конфігурацію

### Значення, що повертаються

### Приклади

**Приклад #2 Приклад використання **Yaf_Application::\_\_construct()****

` <?phpdefined('APPLICATION_PATH')                   // APPLICATION_PATH will be used in the ini config file   | define('APPLICATION_PATH', __DIR__));$application = new Yaf_Application(APPLICATION_PATH.'/conf/application.ini');$application->bootstrap()->run();?> `

Результатом виконання цього прикладу буде щось подібне:

**Приклад #3 Приклад використання **Yaf_Application::\_\_construct()****

`<?php$config = array(    "application" => array(       "directory" => realpath(dirname(__FILE__)) . "/application", Y_ ) $config);$application->bootstrap()->run();?> `

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

- [Yaf_Config_Ini](class.yaf-config-ini.md)
