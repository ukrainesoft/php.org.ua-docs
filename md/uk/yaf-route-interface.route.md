Надсилання запиту

-   [« YafRouteInterface::assemble](yaf-route-interface.assemble.html)
    
-   [YafRouteMap »](class.yaf-route-map.html)
    
-   [PHP Manual](index.md)
    
-   [YafRouteInterface](class.yaf-route-interface.html)
    
-   Надсилання запиту
    

# YafRouteInterface::route

(Yaf >=1.0.0)

YafRouteInterface::route — Надсилання запиту

### Опис

```methodsynopsis
abstract public Yaf_Route_Interface::route(Yaf_Request_Abstract $request): bool
```

**YafRouteInterface::route()** - це єдиний метод, який повинен реалізовувати маршрут користувача.

> **Зауваження**
> 
> починаючи з 2.3.0, має бути реалізований ще один метод, дивіться [YafRouteInterface::assemble()](yaf-route-interface.assemble.html)

Якщо метод повертає **`true`**, Тоді процес маршруту буде завершено. В іншому випадку [YafRouter](class.yaf-router.html) Викликає наступний маршрут у стеку маршрутів для запиту маршруту.

Цей метод встановить результат маршруту для запиту параметра, викликавши [YafRequestAbstract::setControllerName()](yaf-request-abstract.setcontrollername.html) [YafRequestAbstract::setActionName()](yaf-request-abstract.setactionname.html) і [YafRequestAbstract::setModuleName()](yaf-request-abstract.setmodulename.html)

Метод повинен також викликати [YafRequestAbstract::setRouted()](yaf-request-abstract.setrouted.html)щоб запит нарешті був перенаправлений.

### Список параметрів

`request`

Екземпляр [YafRequestAbstract](class.yaf-request-abstract.html)

### Значення, що повертаються