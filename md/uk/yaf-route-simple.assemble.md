---
navigation:
  - class.yaf-route-simple.md: « YafRouteSimple
  - yaf-route-simple.construct.md: 'YafRouteSimple::construct »'
  - index.md: PHP Manual
  - class.yaf-route-simple.md: YafRouteSimple
title: 'YafRouteSimple::assemble'
---
# YafRouteSimple::assemble

(Yaf >=2.3.0)

YafRouteSimple::assemble — Збирає URL

### Опис

```methodsynopsis
public Yaf_Route_Simple::assemble(array $info, array $query = ?): string
```

Збирає URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string).

### Помилки

Викидає [YafExceptionTypeError](class.yaf-exception-typeerror.md), якщо ключі параметра `info` `':c'` ор `':a'` не задані.

### Приклади

**Приклад #1 Приклад використання **YafRouteSimple::assemble()****

```php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Simple('m', 'c', 'a');

$router->addRoute("simple", $route);

var_dump($router->getRoute('simple')->assemble(
            array(
                ':a' => 'yafaction',
                'tkey' => 'tval',
                ':c' => 'yafcontroller',
                ':m' => 'yafmodule'
                ),
            array(
                'tkey1' => 'tval1',
                'tkey2' => 'tval2'
                )
            ));
```

Результатом виконання цього прикладу буде щось подібне:

```
string(64) "?m=yafmodule&c=yafcontroller&a=yafaction&tkey1=tval1&tkey2=tval2"
```
