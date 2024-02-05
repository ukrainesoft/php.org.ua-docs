---
navigation:
  - class.yaf-route-simple.md: « Yaf\_Route\_Simple
  - yaf-route-simple.construct.md: 'Yaf\_Route\_Simple::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-route-simple.md: Yaf\_Route\_Simple
title: 'Yaf\_Route\_Simple::assemble'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Simple::assemble

(Yaf >=2.3.0)

Yaf\_Route\_Simple::assemble — Збирає URL

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

Викидає [Yaf\_Exception\_TypeError](class.yaf-exception-typeerror.md), якщо ключі параметра `info` `':c'`or`':a'` не задані.

### Приклади

**Приклад #1 Приклад використання** Yaf\_Route\_Simple::assemble()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
string(64) "?m=yafmodule&c=yafcontroller&a=yafaction&tkey1=tval1&tkey2=tval2"
```
