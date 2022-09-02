---
navigation:
  - class.yaf-route-interface.md: « YafRouteInterface
  - yaf-route-interface.route.md: 'YafRouteInterface::route »'
  - index.md: PHP Manual
  - class.yaf-route-interface.md: YafRouteInterface
title: 'YafRouteInterface::assemble'
---
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
