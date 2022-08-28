Додає налаштовані маршрути до маршрутизатора

-   [« Yaf\_Router](class.yaf-router.html)
    
-   [Yaf\_Router::addRoute »](yaf-router.addroute.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Router](class.yaf-router.html)
    
-   Додає налаштовані маршрути до маршрутизатора
    

# YafRouter::addConfig

(Yaf >=1.0.0)

YafRouter::addConfig — Додає налаштовані маршрути до маршрутизатора

### Опис

```methodsynopsis
public Yaf_Router::addConfig(Yaf_Config_Abstract $config): bool
```

Додає маршрути, визначені конфігураціями, у стек маршрутів [Yaf\_Router](class.yaf-router.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр [Yaf\_Config\_Abstract](class.yaf-config-abstract.html), який повинен містити одну або кілька допустимих конфігурацій маршруту

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

-   [Yaf\_Router::addRoute()](yaf-router.addroute.html) - Додає новий маршрут до маршрутизатора
-   [Yaf\_Route\_Static](class.yaf-route-static.html)
-   [Yaf\_Route\_Supervar](class.yaf-route-supervar.html)
-   [Yaf\_Route\_Simple](class.yaf-route-simple.html)
-   [Yaf\_Route\_Regex](class.yaf-route-regex.html)
-   [Yaf\_Route\_Rewrite](class.yaf-route-rewrite.html)
-   [Yaf\_Route\_Map](class.yaf-route-map.html)