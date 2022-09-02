---
navigation:
  - yaf-route-simple.assemble.md: '« YafRouteSimple::assemble'
  - yaf-route-simple.route.md: 'YafRouteSimple::route »'
  - index.md: PHP Manual
  - class.yaf-route-simple.md: YafRouteSimple
title: 'YafRouteSimple::construct'
---
# YafRouteSimple::construct

(Yaf >=1.0.0)

YafRouteSimple::construct - Конструктор класу YafRouteSimple

### Опис

public **YafRouteSimple::construct**(string `$module_name`, string `$controller_name`, string `$action_name`

[YafRouteSimple](class.yaf-route-simple.md) отримає інформацію про маршрут з рядка запиту та параметри конструктора будуть використовуватись як ключі при пошуку інформації про маршрут у $GET.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`module_name`

Ім'я ключа інформації про модуль.

`controller_name`

Ім'я ключа інформації про контролера.

`action_name`

Ім'я ключа інформації про дію.

### Значення, що повертаються

Завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання [YafRouteSimple::route()](yaf-route-simple.route.md)**

```php
<?php
   $route = new Yaf_Route_Simple("m", "controller", "act");
   Yaf_Router::getInstance()->addRoute("simple", $route);
?>
```

**Приклад #2 Приклад використання [YafRouteSimple::route()](yaf-route-simple.route.md)**

Запит: [http://yourdomain.com/path/?controller=a&act=b](http://yourdomain.com/path/?controller=a&act=b)\=> module = default(index), controller = a, action = b

Запит: [http://yourdomain.com/path](http://yourdomain.com/path)\=> module = default(index), controller = default(index), action = default(index)

### Дивіться також

-   [YafRouteSupervar::route()](yaf-route-supervar.route.md) - Призначення route
-   [YafRouteStatic::route()](yaf-route-static.route.md) - Надсилає запит
-   [YafRouteRegex::route()](yaf-route-regex.route.md) - Мета маршруту
-   [YafRouteRewrite::route()](yaf-route-rewrite.route.md) - Призначення route
-   [YafRouteMap::route()](yaf-route-map.route.md) - Призначення route
