---
navigation:
  - class.yaf-route-regex.md: « Yaf\_Route\_Regex
  - yaf-route-regex.construct.md: 'Yaf\_Route\_Regex::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-route-regex.md: Yaf\_Route\_Regex
title: 'Yaf\_Route\_Regex::assemble'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Regex::assemble

(Yaf >=2.3.0)

Yaf\_Route\_Regex::assemble — Сформувати URL-адресу

### Опис

```methodsynopsis
public Yaf_Route_Regex::assemble(array $info, array $query = ?): ?string
```

Сформувати URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string) у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Yaf\_Route\_Regex::assemble()\*\*\*\*

```php
<?php

$router = new Yaf_Router();

$route  = new Yaf_Route_Regex(
            "#^/product/([^/]+)/([^/])+#",
            array(
                'controller' => "product",  //маршрут на контроллер product,
                ),
            array(),
            array(),
            '/:m/:c/:a'
        );

$router->addRoute("regex", $route);

var_dump($router->getRoute('regex')->assemble(
            array(
                ':m' => 'module',
                ':c' => 'controller',
                ':a' => 'action'
                ),
            array(
                'tkey1' => 'tval1',
                'tkey2' =>
                'tval2'
                )
            )
        );
```

Висновок наведеного прикладу буде схожим на:

```
string(49) "/module/controller/action?tkey1=tval1&tkey2=tval2"
```
