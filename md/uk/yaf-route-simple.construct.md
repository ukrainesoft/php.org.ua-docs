Конструктор класу YafRouteSimple

-   [« YafRouteSimple::assemble](yaf-route-simple.assemble.html)
    
-   [YafRouteSimple::route »](yaf-route-simple.route.html)
    
-   [PHP Manual](index.html)
    
-   [YafRouteSimple](class.yaf-route-simple.html)
    
-   Конструктор класу YafRouteSimple
    

# YafRouteSimple::construct

(Yaf >=1.0.0)

YafRouteSimple::construct - Конструктор класу YafRouteSimple

### Опис

public **YafRouteSimple::construct**(string `$module_name`, string `$controller_name`, string `$action_name`

[YafRouteSimple](class.yaf-route-simple.html) отримає інформацію про маршрут з рядка запиту та параметри конструктора будуть використовуватись як ключі при пошуку інформації про маршрут у $GET.

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

**Приклад #1 Приклад використання [YafRouteSimple::route()](yaf-route-simple.route.html)**

```php
<?php
   $route = new Yaf_Route_Simple("m", "controller", "act");
   Yaf_Router::getInstance()->addRoute("simple", $route);
?>
```

**Приклад #2 Приклад використання [YafRouteSimple::route()](yaf-route-simple.route.html)**

Запит: [http://yourdomain.com/path/?controller=a&act=b](http://yourdomain.com/path/?controller=a&act=b)\=> module = default(index), controller = a, action = b

Запит: [http://yourdomain.com/path](http://yourdomain.com/path)\=> module = default(index), controller = default(index), action = default(index)

### Дивіться також

-   [YafRouteSupervar::route()](yaf-route-supervar.route.html) - Призначення route
-   [YafRouteStatic::route()](yaf-route-static.route.html) - Надсилає запит
-   [YafRouteRegex::route()](yaf-route-regex.route.html) - Мета маршруту
-   [YafRouteRewrite::route()](yaf-route-rewrite.route.html) - Призначення route
-   [YafRouteMap::route()](yaf-route-map.route.html) - Призначення route