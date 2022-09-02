---
navigation:
  - class.mongodb-bson-timestampinterface.md: « MongoDBBSONTimestampInterface
  - mongodb-bson-timestampinterface.gettimestamp.md: 'MongoDBBSONTimestampInterface::getTimestamp »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestampinterface.md: MongoDBBSONTimestampInterface
title: 'MongoDBBSONTimestampInterface::getIncrement'
---
# MongoDBBSONTimestampInterface::getIncrement

(mongodb >=1.3.0)

MongoDBBSONTimestampInterface::getIncrement — Повертає інкрементний компонент TimestampInterface

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

-   [MongoDBBSONTimestamp::getIncrement()](mongodb-bson-timestamp.getincrement.md) - Повертає компонент збільшення Timestamp
