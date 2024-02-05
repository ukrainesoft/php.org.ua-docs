---
navigation:
  - mongodb-driver-readpreference.construct.md: '« MongoDB\\Driver\\ReadPreference::\_\_construct'
  - mongodb-driver-readpreference.getmaxstalenessseconds.md: 'MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds »'
  - index.md: PHP Manual
  - class.mongodb-driver-readpreference.md: MongoDB\\Driver\\ReadPreference
title: 'MongoDB\\Driver\\ReadPreference::getHedge'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\ReadPreference::getHedge

(mongodb >=1.8.0)

MongoDB\\Driver\\ReadPreference::getHedge — Повертає опцію "hedge" із ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getHedge(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "hedge" із ReadPreference.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [» документація по Read Preference](https://www.mongodb.com/docs/manual/core/read-preference/)
