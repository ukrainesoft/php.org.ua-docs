---
navigation:
  - class.yaf-route-supervar.html: « YafRouteSupervar
  - yaf-route-supervar.construct.html: 'YafRouteSupervar::construct »'
  - index.md: PHP Manual
  - class.yaf-route-supervar.html: YafRouteSupervar
title: 'YafRouteSupervar::assemble'
---
# YafRouteSupervar::assemble

(Yaf >=2.3.0)

YafRouteSupervar::assemble — Збирає URL

### Опис

```methodsynopsis
public Yaf_Route_Supervar::assemble(array $info, array $query = ?): string
```

Збирає URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string).

### Помилки

Викидає [YafExceptionTypeError](class.yaf-exception-typeerror.html), якщо ключі параметра `info` `':c'` and `':a'` не задані.

### Приклади

**Приклад #1 Приклад використання **YafRouteSupervar::assemble()****

```php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Supervar('r');

$router->addRoute("supervar", $route);

var_dump($router->getRoute('supervar')->assemble(
        array(
              ':a' => 'yafaction',
              'tkey' => 'tval',
              ':c' => 'yafcontroller',
              ':m' => 'yafmodule'
        ),
        array(
              'tkey1' => 'tval1',
              'tkey2' => 'tval2'
        )
));

try {
var_dump($router->getRoute('supervar')->assemble(
        array(
              ':a' => 'yafaction',
              'tkey' => 'tval',
              ':m' => 'yafmodule'
        ),
        array(
              'tkey1' => 'tval1',
              'tkey2' => 'tval2',
              1 => array(),
        )
));
} catch (Exception $e) {
    var_dump($e->getMessage());
}
```

Результатом виконання цього прикладу буде щось подібне:

```
string(%d) "?r=/yafmodule/yafcontroller/yafaction&tkey1=tval1&tkey2=tval2"
string(%d) "You need to specify the controller by ':c'"
```
