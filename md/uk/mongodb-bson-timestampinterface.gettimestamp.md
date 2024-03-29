---
navigation:
  - mongodb-bson-timestampinterface.getincrement.md: '« MongoDB\\BSON\\TimestampInterface::getIncrement'
  - mongodb-bson-timestampinterface.tostring.md: 'MongoDB\\BSON\\TimestampInterface::\_\_toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestampinterface.md: MongoDB\\BSON\\TimestampInterface
title: 'MongoDB\\BSON\\TimestampInterface::getTimestamp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\TimestampInterface::getTimestamp

(mongodb >=1.3.0)

MongoDB\\BSON\\TimestampInterface::getTimestamp — Повертає компонент позначки часу TimestampInterface

### Опис

```methodsynopsis
abstract public MongoDB\BSON\TimestampInterface::getTimestamp(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає компонент позначки часу TimestampInterface.

**Увага**

У 32-бітових системах цей метод може повертати негативне число. Хоча частини збільшення та позначки часу типу позначки часу BSON складаються з двох 32-розрядних значень без знака, PHP не може представляти їх на 32-розрядних платформах.

### Дивіться також

-   [MongoDB\\BSON\\Timestamp::getTimestamp()](mongodb-bson-timestamp.gettimestamp.md) \- Повертає компонент позначки часу Timestamp
