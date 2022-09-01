---
navigation:
  - mongodb-driver-serverdescription.gethost.html: '« MongoDBDriverServerDescription::getHost'
  - mongodb-driver-serverdescription.getport.html: 'MongoDBDriverServerDescription::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.html: MongoDBDriverServerDescription
title: 'MongoDBDriverServerDescription::getLastUpdateTime'
---
# MongoDBDriverServerDescription::getLastUpdateTime

(mongodb >=1.13.0)

MongoDBDriverServerDescription::getLastUpdateTime — Повертає час останнього оновлення сервера в мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getLastUpdateTime(): int
```

Повертає час останнього оновлення сервера у мікросекундах.

> **Зауваження**: Значення, що повертається являє собою монотонну мітку часу, яка починається в довільній точці. Як таке, воно підходить тільки для порівняння з іншими значеннями, що повертаються з функції **MongoDBDriverServerDescription::getLastUpdateTime()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останнього оновлення сервера у мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
