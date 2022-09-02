---
navigation:
  - mongodb-bson-timestampinterface.getincrement.md: '« MongoDBBSONTimestampInterface::getIncrement'
  - mongodb-bson-timestampinterface.tostring.md: 'MongoDBBSONTimestampInterface::toString »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestampinterface.md: MongoDBBSONTimestampInterface
title: 'MongoDBBSONTimestampInterface::getTimestamp'
---
# MongoDBBSONTimestampInterface::getTimestamp

(mongodb >=1.3.0)

MongoDBBSONTimestampInterface::getTimestamp — Повертає компонент позначки часу TimestampInterface

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

-   [MongoDBBSONTimestamp::getTimestamp()](mongodb-bson-timestamp.gettimestamp.md) - Повертає компонент позначки часу Timestamp
