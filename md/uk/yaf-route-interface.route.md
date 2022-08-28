Надсилання запиту

-   [« Yaf\_Route\_Interface::assemble](yaf-route-interface.assemble.html)
    
-   [Yaf\_Route\_Map »](class.yaf-route-map.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Route\_Interface](class.yaf-route-interface.html)
    
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
> починаючи з 2.3.0, має бути реалізований ще один метод, дивіться [Yaf\_Route\_Interface::assemble()](yaf-route-interface.assemble.html)

Якщо метод повертає **`true`**, Тоді процес маршруту буде завершено. В іншому випадку [Yaf\_Router](class.yaf-router.html) Викликає наступний маршрут у стеку маршрутів для запиту маршруту.

Цей метод встановить результат маршруту для запиту параметра, викликавши [Yaf\_Request\_Abstract::setControllerName()](yaf-request-abstract.setcontrollername.html) [Yaf\_Request\_Abstract::setActionName()](yaf-request-abstract.setactionname.html) і [Yaf\_Request\_Abstract::setModuleName()](yaf-request-abstract.setmodulename.html)

Метод повинен також викликати [Yaf\_Request\_Abstract::setRouted()](yaf-request-abstract.setrouted.html)щоб запит нарешті був перенаправлений.

### Список параметрів

`request`

Екземпляр [Yaf\_Request\_Abstract](class.yaf-request-abstract.html)

### Значення, що повертаються