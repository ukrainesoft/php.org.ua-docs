- [«Yaf_Router](class.yaf-router.md)
- [Yaf_Router::addRoute »](yaf-router.addroute.md)

- [PHP Manual](index.md)
- [Yaf_Router](class.yaf-router.md)
- Додає настроєні маршрути до маршрутизатора

# Yaf_Router::addConfig

(Yaf \>=1.0.0)

Yaf_Router::addConfig — Додає настроєні маршрути до маршрутизатора

### Опис

public
**Yaf_Router::addConfig**([Yaf_Config_Abstract](class.yaf-config-abstract.md)
`$config`): bool

Додає маршрути, визначені конфігураціями, у стек маршрутів
[Yaf_Router](class.yaf-router.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Примірник [Yaf_Config_Abstract](class.yaf-config-abstract.md), який
повинен містити одну або кілька допустимих конфігурацій маршруту

### Приклади

**Приклад #1 Приклад використання **application.ini()****

`` inicode
порядок дуже важливий, попередній буде названий першим

;запит на переписування маршруту /product/*/*
routes.route_name.type="rewrite"
routes.route_name.match="/product/:name/:value"
routes.route_name.route.controller=product
routes.route_name.route.action=info

;запит відповідності регулярного вираження /list/*/*
routes.route_name1.type="regex"
routes.route_name1.match="#^list/([^/]*)/([^/]*)#"
routes.route_name1.route.controller=Index
routes.route_name1.route.action=action
routes.route_name1.map.1=name
routes.route_name1.map.2=value

;проста відповідність маршруту /**?c=controller&a=action&m=module
routes.route_name2.type="simple"
routes.route_name2.controller=c
routes.route_name2.module=m
routes.route_name2.action=a

;проста відповідність маршрутизатора /**?r=PATH_INFO
routes.route_name3.type="supervar"
routes.route_name3.varname=r

;карта маршруту відповідає будь-якому запиту до контролера
routes.route_name4.type="map"
routes.route_name4.controllerPrefer=TRUE
routes.route_namer.delimiter="#!"
````

**Приклад #2 Приклад використання **Yaf_Dispatcher::autoConfig()****

`<?phpclass Bootstrap extends Yaf_Bootstrap_Abstract{    public function _initConfig() {       $config = Yaf_Application::app()->getConf Yaf_Registry::set("config", $config); }    public function _initRoute(Yaf_Dispatcher $dispatcher) {        $router =$$dispatcher->getRouter(); /**         * ми ми можемо додати кілька визначених маршрутів в application.ini         || }?> `

### Дивіться також

- [Yaf_Router::addRoute()](yaf-router.addroute.md) - Додає новий
маршрут у маршрутизатор
- [Yaf_Route_Static](class.yaf-route-static.md)
- [Yaf_Route_Supervar](class.yaf-route-supervar.md)
- [Yaf_Route_Simple](class.yaf-route-simple.md)
- [Yaf_Route_Regex](class.yaf-route-regex.md)
- [Yaf_Route_Rewrite](class.yaf-route-rewrite.md)
- [Yaf_Route_Map](class.yaf-route-map.md)
