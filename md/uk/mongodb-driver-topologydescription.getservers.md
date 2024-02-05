---
navigation:
  - class.mongodb-driver-topologydescription.md: « MongoDB\\Driver\\TopologyDescription
  - mongodb-driver-topologydescription.gettype.md: 'MongoDB\\Driver\\TopologyDescription::getType »'
  - index.md: PHP Manual
  - class.mongodb-driver-topologydescription.md: MongoDB\\Driver\\TopologyDescription
title: 'MongoDB\\Driver\\TopologyDescription::getServers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\TopologyDescription::getServers

(mongodb >=1.13.0)

MongoDB\\Driver\\TopologyDescription::getServers — Повертає сервери у топології

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::getServers(): array
```

Повертає масив об'єктів [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.md), що відповідають відомим серверам у топології.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив об'єктів [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.md), що відповідають відомим серверам у топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
