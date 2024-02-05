---
navigation:
  - mongodb-driver-topologydescription.gettype.md: '« MongoDB\\Driver\\TopologyDescription::getType'
  - mongodb-driver-topologydescription.haswritableserver.md: 'MongoDB\\Driver\\TopologyDescription::hasWritableServer »'
  - index.md: PHP Manual
  - class.mongodb-driver-topologydescription.md: MongoDB\\Driver\\TopologyDescription
title: 'MongoDB\\Driver\\TopologyDescription::hasReadableServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\TopologyDescription::hasReadableServer

(mongodb >=1.13.0)

MongoDB\\Driver\\TopologyDescription::hasReadableServer — Повертає, чи є в топології сервер, доступний для читання

### Опис

```methodsynopsis
final public MongoDB\Driver\TopologyDescription::hasReadableServer(?MongoDB\Driver\ReadPreference $readPreference = null): bool
```

Повертає, чи є в топології сервер, доступний для читання, або якщо зазначено параметр `readPreference`, сервер, що відповідає вказаній перевагі читання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає, чи є в топології сервер, доступний для читання, або якщо зазначено параметр `readPreference`, сервер, що відповідає вказаній перевагі читання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
