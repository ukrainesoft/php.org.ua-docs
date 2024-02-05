---
navigation:
  - yaf-route-interface.assemble.md: '« Yaf\_Route\_Interface::assemble'
  - class.yaf-route-map.md: Yaf\_Route\_Map »
  - index.md: PHP Manual
  - class.yaf-route-interface.md: Yaf\_Route\_Interface
title: 'Yaf\_Route\_Interface::route'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Interface::route

(Yaf >=1.0.0)

Yaf\_Route\_Interface::route — Надсилання запиту

### Опис

```methodsynopsis
abstract public Yaf_Route_Interface::route(Yaf_Request_Abstract $request): bool
```

**Yaf\_Route\_Interface::route()** - це єдиний метод, який повинен реалізовувати маршрут користувача.

> **Зауваження** :
> 
> починаючи з 2.3.0, має бути реалізований ще один метод, дивіться [Yaf\_Route\_Interface::assemble()](yaf-route-interface.assemble.md)

Якщо метод повертає **`true`**, Тоді процес маршруту буде завершено. В іншому випадку [Yaf\_Router](class.yaf-router.md) Викликає наступний маршрут у стеку маршрутів для запиту маршруту.

Цей метод встановить результат маршруту для запиту параметра, викликавши [Yaf\_Request\_Abstract::setControllerName()](yaf-request-abstract.setcontrollername.md) [Yaf\_Request\_Abstract::setActionName()](yaf-request-abstract.setactionname.md) і [Yaf\_Request\_Abstract::setModuleName()](yaf-request-abstract.setmodulename.md)

Метод повинен також викликати [Yaf\_Request\_Abstract::setRouted()](yaf-request-abstract.setrouted.md)щоб запит нарешті був перенаправлений.

### Список параметрів

`request`

Екземпляр [Yaf\_Request\_Abstract](class.yaf-request-abstract.md)

### Значення, що повертаються
