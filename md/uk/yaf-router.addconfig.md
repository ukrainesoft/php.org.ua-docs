---
navigation:
  - class.yaf-router.md: « Yaf\_Router
  - yaf-router.addroute.md: 'Yaf\_Router::addRoute »'
  - index.md: PHP Manual
  - class.yaf-router.md: Yaf\_Router
title: 'Yaf\_Router::addConfig'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Router::addConfig

(Yaf >=1.0.0)

Yaf\_Router::addConfig — Додає налаштовані маршрути до маршрутизатора

### Опис

```methodsynopsis
public Yaf_Router::addConfig(Yaf_Config_Abstract $config): bool
```

Додає маршрути, визначені конфігураціями, у стек маршрутів [Yaf\_Router](class.yaf-router.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр [Yaf\_Config\_Abstract](class.yaf-config-abstract.md), який повинен містити одну або кілька допустимих конфігурацій маршруту

### Приклади

**Пример #1 Пример использования**application.ini()\*\*\*\*

порядок дуже важливий, попередній буде названий першим

;запит на переписування маршруту /product/\* \*routes.route\_name.type="rewrite" routes.route\_name.match="/product/:name/:value" routes.route\_name.route.controller=product routes.route\_name.route.action=info

;запит відповідності регулярного вираження /list/\* \*routes.route\_name1.type="regex" routes.route\_name1.match="#^list/(\[^/\]\*)/(\[^/\]\*)#" routes.route\_name1.route.controller=Index routes.route\_name1.route.action=action routes.route\_name1.map.1=name routes.route\_name1.map.2=value

;проста відповідність маршруту /\*\*?c=controller&a=action&m=module routes.route\_name2.type="simple" routes.route\_name2.controller=c routes.route\_name2.module=m routes.route\_name2.action=a

;проста відповідність маршрутизатора /\*\*?r=PATH\_INFO routes.route\_name3.type="supervar" routes.route\_name3.varname=r

;карта маршруту відповідає будь-якому запиту до контролера routes.route\_name4.type="map" routes.route\_name4.controllerPrefer=TRUE routes.route\_namer.delimiter="#!"

**Пример #2 Пример использования**Yaf\_Dispatcher::autoConfig()\*\*\*\*

```php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract{
    public function _initConfig() {
        $config = Yaf_Application::app()->getConfig();
        Yaf_Registry::set("config", $config);
    }

    public function _initRoute(Yaf_Dispatcher $dispatcher) {
        $router = $dispatcher->getRouter();
        /**
         * мы можем добавить несколько предопределённых маршрутов в application.ini
         */
        $router->addConfig(Yaf_Registry::get("config")->routes);
    }
?>
```

### Дивіться також

-   [Yaf\_Router::addRoute()](yaf-router.addroute.md) \- Додає новий маршрут до маршрутизатора
-   [Yaf\_Route\_Static](class.yaf-route-static.md)
-   [Yaf\_Route\_Supervar](class.yaf-route-supervar.md)
-   [Yaf\_Route\_Simple](class.yaf-route-simple.md)
-   [Yaf\_Route\_Regex](class.yaf-route-regex.md)
-   [Yaf\_Route\_Rewrite](class.yaf-route-rewrite.md)
-   [Yaf\_Route\_Map](class.yaf-route-map.md)
