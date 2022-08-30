Збирає запит

-   [« YafRouteInterface](class.yaf-route-interface.html)
    
-   [YafRouteInterface::route »](yaf-route-interface.route.html)
    
-   [PHP Manual](index.html)
    
-   [YafRouteInterface](class.yaf-route-interface.html)
    
-   Збирає запит
    

# YafRouteInterface::assemble

(Yaf >=2.3.0)

YafRouteInterface::assemble — Збирає запит

### Опис

```methodsynopsis
abstract public Yaf_Route_Interface::assemble(array $info, array $query = ?): string
```

Метод повертає URL відповідно до інформації аргументу та додає рядки запиту до URL відповідно до запиту аргументу.

Маршрут повинен реалізовувати цей метод відповідно до своїх правил і виконувати зворотний процес.

### Список параметрів

`info`

`query`

### Значення, що повертаються