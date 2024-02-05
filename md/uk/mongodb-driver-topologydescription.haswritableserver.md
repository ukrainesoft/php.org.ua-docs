---
navigation:
  - mongodb-driver-topologydescription.hasreadableserver.md: '« MongoDB\\Driver\\TopologyDescription::hasReadableServer'
  - class.mongodb-driver-writeconcernerror.md: MongoDB\\Driver\\WriteConcernError »
  - index.md: PHP Manual
  - class.mongodb-driver-topologydescription.md: MongoDB\\Driver\\TopologyDescription
title: 'MongoDB\\Driver\\TopologyDescription::hasWritableServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\TopologyDescription::hasWritableServer

(mongodb >=1.13.0)

MongoDB\\Driver\\TopologyDescription::hasWritableServer — Повертає, чи є у топології сервер, доступний для запису

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::hasWritableServer(): bool
```

Повертає, чи є у топології сервер, доступний для запису.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає, чи є у топології сервер, доступний для запису.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
