---
navigation:
  - yaf-route-supervar.assemble.html: '« YafRouteSupervar::assemble'
  - yaf-route-supervar.route.html: 'YafRouteSupervar::route »'
  - index.md: PHP Manual
  - class.yaf-route-supervar.html: YafRouteSupervar
title: 'YafRouteSupervar::construct'
---
# YafRouteSupervar::construct

(Yaf >=1.0.0)

YafRouteSupervar::construct - Призначення construct

### Опис

public **YafRouteSupervar::construct**(string `$supervar_name`

[YafRouteSupervar](class.yaf-route-supervar.html) схожий на [YafRouteStatic](class.yaf-route-static.html), Різниця в тому, що [YafRouteSupervar](class.yaf-route-supervar.md) шукатиме інформацію про шлях у рядку запиту, а параметр supervarname є ключем.

### Список параметрів

`supervar_name`

Назва ключа.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafRouteSupervar()****

```php
<?php
   /**
    * Добавление маршрута supervar в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute(
        "name",
        new Yaf_Route_Supervar("r")
    );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/** для запроса: http://yourdomain.com/xx/oo/?r=/ctr/act/var/value
  * будет следующий результат:
  */
  array (
    "module"   => index(default),
    "controller" => ctr,
    "action"     => act,
    "params"     => array(
          "var" => value,
     )
  )
```

### Дивіться також

-   [YafRouter::addRoute()](yaf-router.addroute.md) - Додає новий маршрут до маршрутизатора
-   [YafRouter::addConfig()](yaf-router.addconfig.md) - Додає налаштовані маршрути до маршрутизатора
-   [YafRouteStatic](class.yaf-route-static.md)
-   [YafRouteRegex](class.yaf-route-regex.md)
-   [YafRouteSimple](class.yaf-route-simple.md)
-   [YafRouteRewrite](class.yaf-route-rewrite.md)
-   [YafRouteMap](class.yaf-route-map.md)
