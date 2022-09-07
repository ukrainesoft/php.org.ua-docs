---
navigation:
  - class.yaf-route-rewrite.md: « YafRouteRewrite
  - yaf-route-rewrite.construct.md: 'YafRouteRewrite::construct »'
  - index.md: PHP Manual
  - class.yaf-route-rewrite.md: YafRouteRewrite
title: 'YafRouteRewrite::assemble'
---
# YafRouteRewrite::assemble

(Yaf >=2.3.0)

YafRouteRewrite::assemble — Збирає URL

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

**Приклад #1 Приклад використання **YafRouteRewrite::assemble()****

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

Результатом виконання цього прикладу буде щось подібне:

```
string(57) "/product/foo/bar/tmpkey1/tmpval1/?tkey1=tval1&tkey2=tval2"
```
