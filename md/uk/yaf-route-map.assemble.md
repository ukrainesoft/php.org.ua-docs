---
navigation:
  - class.yaf-route-map.md: « Yaf\_Route\_Map
  - yaf-route-map.construct.md: 'Yaf\_Route\_Map::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-route-map.md: Yaf\_Route\_Map
title: 'Yaf\_Route\_Map::assemble'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Map::assemble

(Yaf >=2.3.0)

Yaf\_Route\_Map::assemble — Збирає URL

### Опис

```methodsynopsis
public Yaf_Route_Map::assemble(array $info, array $query = ?): string
```

Збирає URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string) у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Може викинути [Yaf\_Exception\_TypeError](class.yaf-exception-typeerror.md)

### Приклади

**Пример #1 Пример использования**Yaf\_Route\_Map::assemble()\*\*\*\*

```php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Map();

$router->addRoute("map", $route);

var_dump($router->getRoute('map')->assemble(
                        array(
                                ':c' => 'foo_bar'
                        ),
                        array(
                                'tkey1' => 'tval1',
                                'tkey2' => 'tval2'
                        )
                   )
);

$route = new Yaf_Route_Map(true, '_');
$router->addRoute("map", $route);

var_dump($router->getRoute('map')->assemble(
                        array(
                                ':a' => 'foo_bar'
                        ),
                        array(
                                'tkey1' => 'tval1',
                                'tkey2' => 'tval2'
                        )
                   )
);
```

Висновок наведеного прикладу буде схожим на:

```
string(%d) "/foo/bar?tkey1=tval1&tkey2=tval2"
string(%d) "/foo/bar/_/tkey1/tval1/tkey2/tval2"
```
