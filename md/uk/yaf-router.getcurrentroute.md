Отримує ім'я діючого маршруту

-   [« YafRouter::construct](yaf-router.construct.html)
    
-   [YafRouter::getRoute »](yaf-router.getroute.html)
    
-   [PHP Manual](index.md)
    
-   [YafRouter](class.yaf-router.html)
    
-   Отримує ім'я діючого маршруту
    

# YafRouter::getCurrentRoute

(Yaf >=1.0.0)

YafRouter::getCurrentRoute — Отримує ім'я чинного маршруту

### Опис

```methodsynopsis
public Yaf_Router::getCurrentRoute(): string
```

Отримує ім'я діючого маршруту.

> **Зауваження**
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
class Bootstrap extends Yaf_Bootstrap_Abstract{
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initRoute(Yaf_Dispatcher $dispatcher) {
        $router = $dispatcher->getRouter();
        $rewrite_route  = new Yaf_Route_Rewrite(
            "/product/list/:page",
            array(
                "controller" => "product",
                "action"     => "list",
            )
        );

        $regex_route  = new Yaf_Route_Rewrite(
            "#^/product/info/(\d+)",
            array(
                "controller" => "product",
                "action"     => "info",
            )
        );

        $router->addRoute('rewrite', $rewrite_route)->addRoute('regex', $regex_route);
    }

    /**
     * зарегистрировать плагин
     */
    public function __initPlugins(Yaf_Dispatcher $dispatcher) {
        $dispatcher->registerPlugin(new DummyPlugin());
    }
}
?>
```

**Приклад #2 Плагін Dummy.php (у [application.directory](yaf.appconfig.html#configuration.yaf.directory)/plugins)**

```php
<?php
class DummyPlugin extends Yaf_Plugin_Abstract {

    public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
         var_dump(Yaf_Dispatcher::getInstance()->getRouter()->getCurrentRoute());
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [YafBootstrapAbstract](class.yaf-bootstrap-abstract.html)
-   [YafPluginAbstract](class.yaf-plugin-abstract.html)
-   [YafRouter::addRoute()](yaf-router.addroute.html) - Додає новий маршрут до маршрутизатора