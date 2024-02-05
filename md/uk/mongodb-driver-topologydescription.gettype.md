---
navigation:
  - mongodb-driver-topologydescription.getservers.md: '« MongoDB\\Driver\\TopologyDescription::getServers'
  - mongodb-driver-topologydescription.hasreadableserver.md: 'MongoDB\\Driver\\TopologyDescription::hasReadableServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-topologydescription.md: MongoDB\\Driver\\TopologyDescription
title: 'MongoDB\\Driver\\TopologyDescription::getType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\TopologyDescription::getType

(mongodb >=1.13.0)

MongoDB\\Driver\\TopologyDescription::getType — Повертає рядок, що позначає тип топології

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::getType(): string
```

Повертає рядок (string), що означає тип топології. Значення співвідноситиметься з константою [MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що означає тип топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
