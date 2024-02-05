---
navigation:
  - yaf-route-map.assemble.md: '« Yaf\_Route\_Map::assemble'
  - yaf-route-map.route.md: 'Yaf\_Route\_Map::route »'
  - index.md: PHP Manual
  - class.yaf-route-map.md: Yaf\_Route\_Map
title: 'Yaf\_Route\_Map::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Map::\_\_construct

(Yaf >=1.0.0)

Yaf\_Route\_Map::\_\_construct — Назначение\_\_construct

### Опис

public**Yaf\_Route\_Map::\_\_construct**(string`$controller_prefer` **`false`**, string`$delimiter` = "")

### Список параметрів

`controller_prefer`

Чи повинен результат розглядатися як контролер чи дія

`delimiter`

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Route\_Map()\*\*\*\*

```php
<?php
   /**
    * Добавить карту маршрута в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Map());
?>
```

Висновок наведеного прикладу буде схожим на:

```
/* для http://yourdomain.com/product/foo/bar
 * результатом маршрута будут следующие значения:
 */
array(
  "controller" => "product_foo_bar",
)
```

**Пример #2 Пример использования**Yaf\_Route\_Map()\*\*\*\*

```php
<?php
   /**
    * Добавить карту маршрута в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",
        new Yaf_Route_Map(true, "_"));
?>
```

Висновок наведеного прикладу буде схожим на:

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

**Пример #3 Пример использования**Yaf\_Route\_Map()\*\*\*\*

```php
<?php
   /**
    * Добавьте карту маршрута в стек маршрутов Yaf_Router, вызвав addconfig
    */
    $config = array(
        "name" => array(
           "type"  => "map",         //маршрут Yaf_Route_Map
           "controllerPrefer" => FALSE,
           "delimiter"        => "#!",
           ),
    );
    Yaf_Dispatcher::getInstance()->getRouter()->addConfig(
        new Yaf_Config_Simple($config));
?>
```

### Дивіться також

-   [Yaf\_Router::addRoute()](yaf-router.addroute.md) \- Додає новий маршрут до маршрутизатора
-   [Yaf\_Route\_Static](class.yaf-route-static.md)
-   [Yaf\_Route\_Supervar](class.yaf-route-supervar.md)
-   [Yaf\_Route\_Simple](class.yaf-route-simple.md)
-   [Yaf\_Route\_Regex](class.yaf-route-regex.md)
-   [Yaf\_Route\_Rewrite](class.yaf-route-rewrite.md)
