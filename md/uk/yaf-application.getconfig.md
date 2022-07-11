- [« Yaf_Application::getAppDirectory](yaf-application.getappdirectory.md)
- [Yaf_Application::getDispatcher »](yaf-application.getdispatcher.md)

- [PHP Manual](index.md)
- [Yaf_Application](class.yaf-application.md)
- Отримати екземпляр класу конфігурації

# Yaf_Application::getConfig

(Yaf \>=1.0.0)

Yaf_Application::getConfig — Отримати екземпляр класу конфігурації

### Опис

public **Yaf_Application::getConfig**():
[Yaf_Config_Abstract](class.yaf-config-abstract.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Примірник класу [Yaf_Config_Abstract](class.yaf-config-abstract.md)

### Приклади

**Приклад #1 Приклад використання **Yaf_Application::getConfig()****

`<?php$config = array(   ""application" => array(       "directory" =>>realpath(dirname(__FILE__)) . "/application", Y $config);print_r($application->getConfig());?> `

Результатом виконання цього прикладу буде щось подібне:

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
