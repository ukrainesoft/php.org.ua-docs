Отримати екземпляр класу конфігурації

-   [« Yaf\_Application::getAppDirectory](yaf-application.getappdirectory.html)
    
-   [Yaf\_Application::getDispatcher »](yaf-application.getdispatcher.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Application](class.yaf-application.html)
    
-   Отримати екземпляр класу конфігурації
    

# YafApplication::getConfig

(Yaf >=1.0.0)

YafApplication::getConfig — Отримати екземпляр класу конфігурації

### Опис

```methodsynopsis
public Yaf_Application::getConfig(): Yaf_Config_Abstract
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр класу [Yaf\_Config\_Abstract](class.yaf-config-abstract.html)

### Приклади

**Приклад #1 Приклад використання **YafApplication::getConfig()****

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getConfig());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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