---
navigation:
  - yaf-application.clearlasterror.md: '« Yaf\_Application::clearLastError'
  - yaf-application.destruct.md: 'Yaf\_Application::\_\_destruct »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::\_\_construct

(Yaf >=1.0.0)

Yaf\_Application::\_\_construct - Конструктор класу Yaf\_Application

### Опис

public**Yaf\_Application::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$config`, string`$envrion`

Екземпляр [Yaf\_Application](class.yaf-application.md)

### Список параметрів

`config`

Шлях до конфігураційного ini-файлу або масив з налаштуваннями

Якщо це шлях до ini-файлу, то в ньому має бути розділ з ім'ям [yaf.environ](yaf.configuration.md#ini.yaf.environ), що є за промовчанням "product".

> **Зауваження** :
> 
> Якщо ви використовуєте ini-файл, то для покращення продуктивності дозвольте опцію [yaf.cache\_config](yaf.configuration.md#ini.yaf.cache-config)

Параметри конфігурації (та їх значення за промовчанням):

**Приклад #1 Приклад ini-файлу**

\[product\];Ця опція не має значення за умовчанням і обов'язково має бути задана вами application.directory=APPLICATION\_PATH

;Наступні параметри мають значення за замовчуванням, вам можна їх не чіпати application.library = APPLICATION\_PATH . "/library" application.dispatcher.throwException=1 application.dispatcher.catchException=1

application.baseUri=""

;розширення php-скриптів ap.ext=php

;розширення файлів шаблонів ap.view.ext=phtml

ap.dispatcher.defaultModule=Index ap.dispatcher.defaultController=Index ap.dispatcher.defaultAction=index

;Певні модулі ap.modules=Index

`envrion`

Який розділ буде завантажено як остаточну конфігурацію

### Значення, що повертаються

### Приклади

**Пример #2 Пример использования**Yaf\_Application::\_\_construct()\*\*\*\*

```php
<?php
defined('APPLICATION_PATH')                  // APPLICATION_PATH will be used in the ini config file
    || define('APPLICATION_PATH', __DIR__));

$application = new Yaf_Application(APPLICATION_PATH.'/conf/application.ini');
$application->bootstrap()->run();
?>
```

Висновок наведеного прикладу буде схожим на:

**Пример #3 Пример использования**Yaf\_Application::\_\_construct()\*\*\*\*

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
$application->bootstrap()->run();
?>
```

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Yaf\_Config\_Ini](class.yaf-config-ini.md)
