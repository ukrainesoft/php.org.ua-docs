---
navigation:
  - class.mongodb-bson-timestampinterface.md: « MongoDB\\BSON\\TimestampInterface
  - mongodb-bson-timestampinterface.gettimestamp.md: 'MongoDB\\BSON\\TimestampInterface::getTimestamp »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestampinterface.md: MongoDB\\BSON\\TimestampInterface
title: 'MongoDB\\BSON\\TimestampInterface::getIncrement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\TimestampInterface::getIncrement

(mongodb >=1.3.0)

MongoDB\\BSON\\TimestampInterface::getIncrement — Повертає інкрементний компонент TimestampInterface

### Опис

```methodsynopsis
abstract public MongoDB\BSON\TimestampInterface::getIncrement(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає інкрементний компонент TimestampInterface.

**Увага**

У 32-бітових системах цей метод може повертати негативне число. Хоча частини збільшення та позначки часу типу позначки часу BSON складаються з двох 32-розрядних значень без знака, PHP не може представляти їх на 32-розрядних платформах.

### Дивіться також

-   [MongoDB\\BSON\\Timestamp::getIncrement()](mongodb-bson-timestamp.getincrement.md) \- Повертає компонент збільшення Timestamp
