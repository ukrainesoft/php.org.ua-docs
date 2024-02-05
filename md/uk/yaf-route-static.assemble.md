---
navigation:
  - class.yaf-route-static.md: « Yaf\_Route\_Static
  - yaf-route-static.match.md: 'Yaf\_Route\_Static::match »'
  - index.md: PHP Manual
  - class.yaf-route-static.md: Yaf\_Route\_Static
title: 'Yaf\_Route\_Static::assemble'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Static::assemble

(Yaf >=2.3.0)

Yaf\_Route\_Static::assemble — Збирає URL

### Опис

```methodsynopsis
public Yaf_Route_Static::assemble(array $info, array $query = ?): string
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

**Приклад #1 Приклад використання** Yaf\_Route\_Static::assemble()\*\*\*\*

```php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Static();

$router->addRoute("static", $route);

var_dump($router->getRoute('static')->assemble(
            array(
                ':a' => 'yafaction',
                'tkey' => 'tval',
                ':c' => 'yafcontroller',
                ':m' => 'yafmodule'
            ),
        )
);

var_dump($router->getRoute('static')->assemble(
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
        )
);
```

Висновок наведеного прикладу буде схожим на:

```
string(%d) "/yafmodule/yafcontroller/yafaction"
string(%d) "/yafmodule/yafcontroller/yafaction?tkey1=tval1&tkey2=tval2"
```
