---
navigation:
  - class.yaf-route-supervar.md: « Yaf\_Route\_Supervar
  - yaf-route-supervar.construct.md: 'Yaf\_Route\_Supervar::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-route-supervar.md: Yaf\_Route\_Supervar
title: 'Yaf\_Route\_Supervar::assemble'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Supervar::assemble

(Yaf >=2.3.0)

Yaf\_Route\_Supervar::assemble — Збирає URL

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

Викидає [Yaf\_Exception\_TypeError](class.yaf-exception-typeerror.md), якщо ключі параметра `info` `':c'`and`':a'` не задані.

### Приклади

**Приклад #1 Приклад використання** Yaf\_Route\_Supervar::assemble()\*\*\*\*

```php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Supervar('r');

$router->addRoute("supervar", $route);

var_dump($router->getRoute('supervar')->assemble(
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

try {
var_dump($router->getRoute('supervar')->assemble(
        array(
              ':a' => 'yafaction',
              'tkey' => 'tval',
              ':m' => 'yafmodule'
        ),
        array(
              'tkey1' => 'tval1',
              'tkey2' => 'tval2',
              1 => array(),
        )
));
} catch (Exception $e) {
    var_dump($e->getMessage());
}
```

Висновок наведеного прикладу буде схожим на:

```
string(%d) "?r=/yafmodule/yafcontroller/yafaction&tkey1=tval1&tkey2=tval2"
string(%d) "You need to specify the controller by ':c'"
```
