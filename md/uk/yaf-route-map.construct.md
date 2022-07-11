- [« Yaf_Route_Map::assemble](yaf-route-map.assemble.md)
- [Yaf_Route_Map::route »](yaf-route-map.route.md)

- [PHP Manual](index.md)
- [Yaf_Route_Map](class.yaf-route-map.md)
- Призначення \_\_construct

# Yaf_Route_Map::\_\_construct

(Yaf \>=1.0.0)

Yaf_Route_Map::\_\_construct - Призначення \_\_construct

### Опис

public **Yaf_Route_Map::\_\_construct**(string `$controller_prefer` =
**`false`**, string `$delimiter` = "")

### Список параметрів

`controller_prefer`
Чи повинен результат розглядатися як контролер чи дія

`delimiter`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Yaf_Route_Map()****

?<?php  |****   ** Додати карту маршрута в стек маршрутів Yaf_Router    */   Yaf_Dispatcher::getInstance()->|

Результатом виконання цього прикладу буде щось подібне:

/* для http://yourdomain.com/product/foo/bar
* результатом маршруту будуть наступні значення:
*/
array(
"controller" => "product_foo_bar",
)

**Приклад #2 Приклад використання **Yaf_Route_Map()****

` <?php   /**    * Добавить карту маршрута в стек маршрутов Yaf_Router    */    Yaf_Dispatcher::getInstance()->getRouter()->addRoute("name",        new Yaf_Route_Map(true, "_"));?> `

Результатом виконання цього прикладу буде щось подібне:

/* для http://yourdomain.com/user/list/_/foo/22
* результатом маршруту будуть наступні значення:
*/
array(
"action" => "user_list",
)

/**
* та параметри запиту:
*/
array(
"foo" => 22,
)

**Приклад #3 Приклад використання **Yaf_Route_Map()****

` <?php   /**    * Добавьте карту маршрута в стек маршрутов Yaf_Router, вызвав addconfig    */    $config = array(        "name" => array(           "type"  => "map",         //маршрут Yaf_Route_Map           "controllerPrefer" => FALSE,      "delimiter"        => "#!",            ),    ); Yaf_Dispatcher::getInstance()->getRouter()->addConfig(        new Yaf_Config_Simple($config));?> `

### Дивіться також

- [Yaf_Router::addRoute()](yaf-router.addroute.md) - Додає новий
маршрут у маршрутизатор
- [Yaf_Route_Static](class.yaf-route-static.md)
- [Yaf_Route_Supervar](class.yaf-route-supervar.md)
- [Yaf_Route_Simple](class.yaf-route-simple.md)
- [Yaf_Route_Regex](class.yaf-route-regex.md)
- [Yaf_Route_Rewrite](class.yaf-route-rewrite.md)
