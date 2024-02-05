---
navigation:
  - class.yaf-route-interface.md: « Yaf\_Route\_Interface
  - yaf-route-interface.route.md: 'Yaf\_Route\_Interface::route »'
  - index.md: PHP Manual
  - class.yaf-route-interface.md: Yaf\_Route\_Interface
title: 'Yaf\_Route\_Interface::assemble'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Interface::assemble

(Yaf >=2.3.0)

Yaf\_Route\_Interface::assemble — Збирає запит

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
