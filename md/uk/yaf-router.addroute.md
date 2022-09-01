---
navigation:
  - yaf-router.addconfig.html: '« YafRouter::addConfig'
  - yaf-router.construct.html: 'YafRouter::construct »'
  - index.md: PHP Manual
  - class.yaf-router.html: YafRouter
title: 'YafRouter::addRoute'
---
# YafRouter::addRoute

(Yaf >=1.0.0)

YafRouter::addRoute — Додає новий маршрут до маршрутизатора

### Опис

```methodsynopsis
public Yaf_Router::addRoute(string $name, Yaf_Route_Abstract $route): bool
```

За замовчуванням, YafRouter використовує [YafRouteStatic](class.yaf-route-static.html) як маршрут за замовчуванням. Ви можете додати нові маршрути до стек маршрутів маршрутизатора, викликавши цей метод.

Новіший маршрут буде викликаний раніше, ніж старий (стек маршрутів), і якщо новий маршрутизатор поверне **`true`**, процес маршрутизатора буде завершено. В іншому випадку буде викликано старіший.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання [YafDispatcher::autoRender()](yaf-dispatcher.autorender.html)**

```php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initRoute(Yaf_Dispatcher $dispatcher) {
        $router = $dispatcher->getRouter();
        /**
         * мы можем добавить несколько предопределённых маршрутов в application.ini
         */
        $router->addConfig(Yaf_Registry::get("config")->routes);
        /**
         * добавьте Rewrite route, затем запрос uri:
         * http://example.com/product/list/22/foo
         * будет соответствовать этому маршруту, и результат:
         *
         *  [module] =>
         *  [controller] => product
         *  [action] => info
         *  [method] => GET
         *  [params:protected] => Array
         *      (
         *          [id] => 22
         *          [name] => foo
         *      )
         *
         */
        $route  = new Yaf_Route_Rewrite(
            "/product/list/:id/:name",
            array(
                "controller" => "product",
                "action"     => "info",
            )
        );

        $router->addRoute('dummy', $route);
    }
}
?>
```

### Дивіться також

-   [YafRouter::addConfig()](yaf-router.addconfig.html) - Додає налаштовані маршрути до маршрутизатора
-   [YafRouteStatic](class.yaf-route-static.html)
-   [YafRouteSupervar](class.yaf-route-supervar.html)
-   [YafRouteSimple](class.yaf-route-simple.html)
-   [YafRouteRegex](class.yaf-route-regex.html)
-   [YafRouteRewrite](class.yaf-route-rewrite.html)
-   [YafRouteMap](class.yaf-route-map.html)
