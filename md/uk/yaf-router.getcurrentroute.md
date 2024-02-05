---
navigation:
  - yaf-router.construct.md: '« Yaf\_Router::\_\_construct'
  - yaf-router.getroute.md: 'Yaf\_Router::getRoute »'
  - index.md: PHP Manual
  - class.yaf-router.md: Yaf\_Router
title: 'Yaf\_Router::getCurrentRoute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Router::getCurrentRoute

(Yaf >=1.0.0)

Yaf\_Router::getCurrentRoute — Отримує ім'я чинного маршруту

### Опис

```methodsynopsis
public Yaf_Router::getCurrentRoute(): string
```

Отримує ім'я діючого маршруту.

> **Зауваження** :
> 
> Ви повинні викликати цей метод після завершення процесу маршрутизації, оскільки до цього цей метод завжди повертатиметься **`null`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок, назва діючого маршруту.

### Приклади

**Приклад #1 Реєстрація деяких маршрутів у Bootstrap**

```php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initRoute(Yaf_Dispatcher $dispatcher) {
        $router = $dispatcher->getRouter();
        $rewrite_route  = new Yaf_Route_Rewrite(
            "/product/list/:page",
            array(
                "controller" => "product",
                "action"     => "list",
            )
        );

        $regex_route  = new Yaf_Route_Rewrite(
            "#^/product/info/(\d+)",
            array(
                "controller" => "product",
                "action"     => "info",
            )
        );

        $router->addRoute('rewrite', $rewrite_route)->addRoute('regex', $regex_route);
    }

    /**
     * зарегистрировать плагин
     */
    public function __initPlugins(Yaf_Dispatcher $dispatcher) {
        $dispatcher->registerPlugin(new DummyPlugin());
    }
}
?>
```

**Приклад #2 Плагин Dummy.php (в[application.directory](yaf.appconfig.md#configuration.yaf.directory)/plugins)**

```php
<?php
class DummyPlugin extends Yaf_Plugin_Abstract {

    public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
         var_dump(Yaf_Dispatcher::getInstance()->getRouter()->getCurrentRoute());
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
/* для http://yourdomain.com/product/list/1
 * DummyPlugin выведет:
 */
string(7) "rewrite"

/* для http://yourdomain.com/product/info/34
 * DummyPlugin выведет:
 */
string(5) "regex"

/* для другого запроса URI
 * DummyPlugin выведет:
 */
string(8) "_default"
```

### Дивіться також

-   [Yaf\_Bootstrap\_Abstract](class.yaf-bootstrap-abstract.md)
-   [Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.md)
-   [Yaf\_Router::addRoute()](yaf-router.addroute.md) \- Додає новий маршрут до маршрутизатора
