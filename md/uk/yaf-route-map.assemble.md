---
navigation:
  - class.yaf-route-map.md: « YafRouteMap
  - yaf-route-map.construct.md: 'YafRouteMap::construct »'
  - index.md: PHP Manual
  - class.yaf-route-map.md: YafRouteMap
title: 'YafRouteMap::assemble'
---
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

Може викинути [YafExceptionTypeError](class.yaf-exception-typeerror.md)

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
