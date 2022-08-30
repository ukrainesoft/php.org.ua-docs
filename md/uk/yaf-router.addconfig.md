Додає налаштовані маршрути до маршрутизатора

-   [« YafRouter](class.yaf-router.html)
    
-   [YafRouter::addRoute »](yaf-router.addroute.html)
    
-   [PHP Manual](index.md)
    
-   [YafRouter](class.yaf-router.html)
    
-   Додає налаштовані маршрути до маршрутизатора
    

# YafRouter::addConfig

(Yaf >=1.0.0)

YafRouter::addConfig — Додає налаштовані маршрути до маршрутизатора

### Опис

```methodsynopsis
public Yaf_Router::addConfig(Yaf_Config_Abstract $config): bool
```

Додає маршрути, визначені конфігураціями, у стек маршрутів [YafRouter](class.yaf-router.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр [YafConfigAbstract](class.yaf-config-abstract.html), який повинен містити одну або кілька допустимих конфігурацій маршруту

### Приклади

**Приклад #1 Приклад використання **application.ini()****

порядок дуже важливий, попередній буде названий першим

;запит на переписування маршруту /product/routes.routename.type="rewrite" routes.routename.match="/product/:name/:value" routes.routename.route.controller=product routes.routename.route.action=info

;запит відповідності регулярного вираження /list/routes.routename1.type="regex" routes.routename1.match="#^list/()#" routes.routename1.route.controller=Index routes.routename1.route.action=action routes.routename1.map.1=name routes.routename1.map.2=value

;проста відповідність маршруту /?c=controller&a=action&m=module routes.routename2.type="simple" routes.routename2.controller=c routes.routename2.module=m routes.routename2.action=a

;проста відповідність маршрутизатора /?r=PATHINFO routes.routename3.type="supervar" routes.routename3.varname=r

;карта маршруту відповідає будь-якому запиту до контролера routes.routename4.type="map" routes.routename4.controllerPrefer=TRUE routes.routenamer.delimiter="#!"

**Приклад #2 Приклад використання **YafDispatcher::autoConfig()****

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
    }
?>
```

### Дивіться також

-   [YafRouter::addRoute()](yaf-router.addroute.html) - Додає новий маршрут до маршрутизатора
-   [YafRouteStatic](class.yaf-route-static.html)
-   [YafRouteSupervar](class.yaf-route-supervar.html)
-   [YafRouteSimple](class.yaf-route-simple.html)
-   [YafRouteRegex](class.yaf-route-regex.html)
-   [YafRouteRewrite](class.yaf-route-rewrite.html)
-   [YafRouteMap](class.yaf-route-map.html)