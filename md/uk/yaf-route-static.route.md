Надсилає запит

-   [« YafRouteStatic::match](yaf-route-static.match.html)
    
-   [YafRouteSupervar »](class.yaf-route-supervar.html)
    
-   [PHP Manual](index.html)
    
-   [YafRouteStatic](class.yaf-route-static.html)
    
-   Надсилає запит
    

# YafRouteStatic::route

(Yaf >=1.0.0)

YafRouteStatic::route — Надсилає запит

### Опис

```methodsynopsis
public Yaf_Route_Static::route(Yaf_Request_Abstract $request): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`request`

### Значення, що повертаються

Завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **YafRouteStatic::route()****

// за умови, що визначено лише один модуль: Index Запит: [http://yourdomain.com/a/b](http://yourdomain.com/a/b)\=> module = index, controller = a, action = b

//за умови, що ap.actionprefer = On Запит: [http://yourdomain.com/b](http://yourdomain.com/b)\=> module = default(index), controller = default(index), action = b

//за умови, що ap.actionprefer = Off Запит: [http://yourdomain.com/b](http://yourdomain.com/b)\=> module = default(index), controller = b, action = default(index)

Запит: [http://yourdomain.com/a/b/foo/bar/test/a/id/4](http://yourdomain.com/a/b/foo/bar/test/a/id/4)\=> module = default(index), controller = a, action = b, параметри запиту: foo = bar, test = a, id = 4

### Дивіться також

-   [YafRouteSupervar::route()](yaf-route-supervar.route.html) - Призначення route
-   [YafRouteSimple::route()](yaf-route-simple.route.html) - Надсилає запит
-   [YafRouteRegex::route()](yaf-route-regex.route.html) - Мета маршруту
-   [YafRouteRewrite::route()](yaf-route-rewrite.route.html) - Призначення route
-   [YafRouteMap::route()](yaf-route-map.route.html) - Призначення route