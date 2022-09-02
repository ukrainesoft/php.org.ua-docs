---
navigation:
  - mongodb-driver-topologydescription.getservers.md: '« MongoDBDriverTopologyDescription::getServers'
  - mongodb-driver-topologydescription.hasreadableserver.md: 'MongoDBDriverTopologyDescription::hasReadableServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-topologydescription.md: MongoDBDriverTopologyDescription
title: 'MongoDBDriverTopologyDescription::getType'
---
# MongoDBDriverTopologyDescription::getType

(mongodb >=1.13.0)

MongoDBDriverTopologyDescription::getType — Повертає рядок, що позначає тип топології

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::getType(): string
```

Повертає рядок (string), що означає тип топології. Значення співвідноситиметься з константою [MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що означає тип топології.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
