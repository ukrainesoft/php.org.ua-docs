---
navigation:
  - yaf-application.getappdirectory.md: '« Yaf\_Application::getAppDirectory'
  - yaf-application.getdispatcher.md: 'Yaf\_Application::getDispatcher »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::getConfig'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::getConfig

(Yaf >=1.0.0)

Yaf\_Application::getConfig — Отримати екземпляр класу конфігурації

### Опис

```methodsynopsis
public Yaf_Application::getConfig(): Yaf_Config_Abstract
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр класу [Yaf\_Config\_Abstract](class.yaf-config-abstract.md)

### Приклади

**Приклад #1 Приклад використання** Yaf\_Application::getConfig()\*\*\*\*

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getConfig());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Yaf_Config_Simple Object
(
    [_config:protected] => Array
        (
            [application] => Array
                (
                    [directory] => /home/laruence/local/www/htdocs/application
                )

        )

    [_readonly:protected] => 1
)
```
