Збирає URL

-   [« YafRouteMap](class.yaf-route-map.html)
    
-   [YafRouteMap::construct »](yaf-route-map.construct.html)
    
-   [PHP Manual](index.html)
    
-   [YafRouteMap](class.yaf-route-map.html)
    
-   Збирає URL
    

# YafRouteMap::assemble

(Yaf >=2.3.0)

YafRouteMap::assemble — Збирає URL

### Опис

```methodsynopsis
public Yaf_Route_Map::assemble(array $info, array $query = ?): string
```

Збирає URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string) у разі успішного виконання або **`null`** у разі виникнення помилки.

### Помилки

Може викинути [YafExceptionTypeError](class.yaf-exception-typeerror.html)

### Приклади

**Приклад #1 Приклад використання **YafRouteMap::assemble()****

```php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Map();

$router->addRoute("map", $route);

var_dump($router->getRoute('map')->assemble(
                        array(
                                ':c' => 'foo_bar'
                        ),
                        array(
                                'tkey1' => 'tval1',
                                'tkey2' => 'tval2'
                        )
                   )
);

$route = new Yaf_Route_Map(true, '_');
$router->addRoute("map", $route);

var_dump($router->getRoute('map')->assemble(
                        array(
                                ':a' => 'foo_bar'
                        ),
                        array(
                                'tkey1' => 'tval1',
                                'tkey2' => 'tval2'
                        )
                   )
);
```

Результатом виконання цього прикладу буде щось подібне:

```
string(%d) "/foo/bar?tkey1=tval1&tkey2=tval2"
string(%d) "/foo/bar/_/tkey1/tval1/tkey2/tval2"
```