Мета маршруту

-   [« YafRouteRegex::construct](yaf-route-regex.construct.html)
    
-   [YafRouteRewrite »](class.yaf-route-rewrite.html)
    
-   [PHP Manual](index.html)
    
-   [YafRouteRegex](class.yaf-route-regex.html)
    
-   Мета маршруту
    

# YafRouteRegex::route

(Yaf >=1.0.0)

YafRouteRegex::route — Мета маршруту

### Опис

```methodsynopsis
public Yaf_Route_Regex::route(Yaf_Request_Abstract $request): bool
```

Перенаправити вхідний запит.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`request`

### Значення, що повертаються

Якщо шаблон встановлено першим параметром **YafRouteRegex::construct()** проводить відповідність із запитом URI, повертаючи **`true`**, в іншому випадку - **`false`**