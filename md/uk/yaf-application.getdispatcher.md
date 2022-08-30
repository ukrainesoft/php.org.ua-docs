Отримати екземпляр класу YafDispatcher

-   [« YafApplication::getConfig](yaf-application.getconfig.html)
    
-   [YafApplication::getLastErrorMsg »](yaf-application.getlasterrormsg.html)
    
-   [PHP Manual](index.html)
    
-   [YafApplication](class.yaf-application.html)
    
-   Отримати екземпляр класу YafDispatcher
    

# YafApplication::getDispatcher

(Yaf >=1.0.0)

YafApplication::getDispatcher — Отримати примірник класу YafDispatcher

### Опис

```methodsynopsis
public Yaf_Application::getDispatcher(): Yaf_Dispatcher
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafApplication::getDispatcher()****

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getDispatcher());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Yaf_Dispatcher Object
(
    [_router:protected] => Yaf_Router Object
        (
            [_routes:protected] => Array
                (
                    [_default] => Yaf_Route_Static Object
                        (
                        )

                )

            [_current:protected] =>
        )

    [_view:protected] =>
    [_request:protected] => Yaf_Request_Http Object
        (
            [module] =>
            [controller] =>
            [action] =>
            [method] => Cli
            [params:protected] => Array
                (
                )

            [language:protected] =>
            [_exception:protected] =>
            [_base_uri:protected] =>
            [uri:protected] =>
            [dispatched:protected] =>
            [routed:protected] =>
        )

    [_plugins:protected] => Array
        (
        )

    [_auto_render:protected] => 1
    [_return_response:protected] =>
    [_instantly_flush:protected] =>
    [_default_module:protected] => Index
    [_default_controller:protected] => Index
    [_default_action:protected] => index
    [_response] => Yaf_Response_Cli Object
        (
            [_header:protected] => Array
                (
                )

            [_body:protected] =>
            [_sendheader:protected] =>
        )

)
```