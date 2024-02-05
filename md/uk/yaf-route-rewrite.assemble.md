---
navigation:
  - class.yaf-route-rewrite.md: « Yaf\_Route\_Rewrite
  - yaf-route-rewrite.construct.md: 'Yaf\_Route\_Rewrite::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-route-rewrite.md: Yaf\_Route\_Rewrite
title: 'Yaf\_Route\_Rewrite::assemble'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Rewrite::assemble

(Yaf >=2.3.0)

Yaf\_Route\_Rewrite::assemble — Збирає URL

### Опис

```methodsynopsis
public Yaf_Route_Rewrite::assemble(array $info, array $query = ?): string
```

Збирає URL-адресу.

### Список параметрів

`info`

`query`

### Значення, що повертаються

Повертає рядок (string).

### Приклади

**Пример #1 Пример использования**Yaf\_Route\_Rewrite::assemble()\*\*\*\*

```php
router = new Yaf_Router();

$route  = new Yaf_Route_Rewrite(
                "/product/:name/:id/*",
                array(
                        'controller' => "product",
                ),
                array()
);

$router->addRoute("rewrite", $route);

var_dump($router->getRoute('rewrite')->assemble(
                        array(
                                ':name' => 'foo',
                                ':id' => 'bar',
                                ':tmpkey1' => 'tmpval1'
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
string(57) "/product/foo/bar/tmpkey1/tmpval1/?tkey1=tval1&tkey2=tval2"
```
