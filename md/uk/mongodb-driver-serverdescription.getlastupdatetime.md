---
navigation:
  - mongodb-driver-serverdescription.gethost.md: '« MongoDB\\Driver\\ServerDescription::getHost'
  - mongodb-driver-serverdescription.getport.md: 'MongoDB\\Driver\\ServerDescription::getPort »'
  - index.md: PHP Manual
  - class.mongodb-driver-serverdescription.md: MongoDB\\Driver\\ServerDescription
title: 'MongoDB\\Driver\\ServerDescription::getLastUpdateTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ServerDescription::getLastUpdateTime

(mongodb >=1.13.0)

MongoDB\\Driver\\ServerDescription::getLastUpdateTime — Повертає час останнього оновлення сервера в мікросекундах

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerDescription::getLastUpdateTime(): int
```

Повертає час останнього оновлення сервера у мікросекундах.

> **Зауваження**: Значення, що повертається являє собою монотонну мітку часу, яка починається в довільній точці. Як таке, воно підходить тільки для порівняння з іншими значеннями, що повертаються з функції **MongoDB\\Driver\\ServerDescription::getLastUpdateTime()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останнього оновлення сервера у мікросекундах.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
