---
navigation:
  - yaf-application.getconfig.md: '« Yaf\_Application::getConfig'
  - yaf-application.getlasterrormsg.md: 'Yaf\_Application::getLastErrorMsg »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::getDispatcher'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::getDispatcher

(Yaf >=1.0.0)

Yaf\_Application::getDispatcher — Отримати примірник класу Yaf\_Dispatcher

### Опис

```methodsynopsis
public Yaf_Application::getDispatcher(): Yaf_Dispatcher
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Yaf\_Application::getDispatcher()\*\*\*\*

```php
<?php
$config = array(
    "application" => array(
        "directory" => realpath(dirname(__FILE__)) . "/application",
    ),
);

/** Yaf_Application */
$application = new Yaf_Application($config);
print_r($application->getDispatcher());
?>
```

Висновок наведеного прикладу буде схожим на:

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
