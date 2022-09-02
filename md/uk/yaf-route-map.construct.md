---
navigation:
  - yaf-route-map.assemble.md: '« YafRouteMap::assemble'
  - yaf-route-map.route.md: 'YafRouteMap::route »'
  - index.md: PHP Manual
  - class.yaf-route-map.md: YafRouteMap
title: 'YafRouteMap::construct'
---
# YafRouteMap::construct

(Yaf >=1.0.0)

YafRouteMap::construct - Призначення construct

### Опис

public **YafRouteMap::construct**(string `$controller_prefer` **`false`**, string `$delimiter` = "")

### Список параметрів

`controller_prefer`

Чи повинен результат розглядатися як контролер чи дія

`delimiter`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafRouteMap()****

```php
<?php
   /**
    * Добавить карту маршрута в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Map());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/* для http://yourdomain.com/product/foo/bar
 * результатом маршрута будут следующие значения:
 */
array(
  "controller" => "product_foo_bar",
)
```

**Приклад #2 Приклад використання **YafRouteMap()****

```php
<?php
   /**
    * Добавить карту маршрута в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Map(true, "_"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/* для http://yourdomain.com/user/list/_/foo/22
 * результатом маршрута будут следующие значения::
 */
array(
    "action" => "user_list",
)

/**
 * и параметры запроса:
 */
array(
  "foo"   => 22,
)
```

**Приклад #3 Приклад використання **YafRouteMap()****

```php
<?php
   /**
    * Добавьте карту маршрута в стек маршрутов Yaf_Router, вызвав addconfig
    */
    $config = array(
        "name" => array(
           "type"  => "map",         //маршрут Yaf_Route_Map
           "controllerPrefer" => FALSE,
           "delimiter"        => "#!",
           ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

### Дивіться також

-   [YafRouter::addRoute()](yaf-router.addroute.md) - Додає новий маршрут до маршрутизатора
-   [YafRouteStatic](class.yaf-route-static.md)
-   [YafRouteSupervar](class.yaf-route-supervar.md)
-   [YafRouteSimple](class.yaf-route-simple.md)
-   [YafRouteRegex](class.yaf-route-regex.md)
-   [YafRouteRewrite](class.yaf-route-rewrite.md)
