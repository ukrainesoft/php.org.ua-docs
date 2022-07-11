- [« Yaf_Application::getConfig](yaf-application.getconfig.md)
- [Yaf_Application::getLastErrorMsg »](yaf-application.getlasterrormsg.md)

- [PHP Manual](index.md)
- [Yaf_Application](class.yaf-application.md)
- Отримати екземпляр класу Yaf_Dispatcher

# Yaf_Application::getDispatcher

(Yaf \>=1.0.0)

Yaf_Application::getDispatcher — Отримати примірник класу
Yaf_Dispatcher

### Опис

public **Yaf_Application::getDispatcher**():
[Yaf_Dispatcher](class.yaf-dispatcher.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Yaf_Application::getDispatcher()****

`<?php$config = array(    "application" => array(       "directory" => realpath(dirname(__FILE__)) . "/application", Y_ ) $config);print_r($application->getDispatcher());?> `

Результатом виконання цього прикладу буде щось подібне:

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
