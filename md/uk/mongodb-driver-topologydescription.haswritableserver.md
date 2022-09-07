---
navigation:
  - mongodb-driver-topologydescription.hasreadableserver.md: '« MongoDBDriverTopologyDescription::hasReadableServer'
  - class.mongodb-driver-writeconcernerror.md: MongoDBDriverWriteConcernError »
  - index.md: PHP Manual
  - class.mongodb-driver-topologydescription.md: MongoDBDriverTopologyDescription
title: 'MongoDBDriverTopologyDescription::hasWritableServer'
---
# MongoDBDriverTopologyDescription::hasWritableServer

(mongodb >=1.13.0)

MongoDBDriverTopologyDescription::hasWritableServer — Повертає, чи є у топології сервер, доступний для запису

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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
