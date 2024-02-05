---
navigation:
  - mongodb-bson-timestamp.getincrement.md: '« MongoDB\\BSON\\Timestamp::getIncrement'
  - mongodb-bson-timestamp.jsonserialize.md: 'MongoDB\\BSON\\Timestamp::jsonSerialize »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.md: MongoDB\\BSON\\Timestamp
title: 'MongoDB\\BSON\\Timestamp::getTimestamp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Timestamp::getTimestamp

(mongodb >=1.3.0)

MongoDB\\BSON\\Timestamp::getTimestamp — Повертає компонент позначки часу Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::getTimestamp(): int
```

Компонент позначки часу Timestamp – це його найбільш значущі 32 біти, які позначають кількість секунд від початку епохи Unix. Це значення читається як 32-розрядне ціле число без знака з порядком байтів у старшому порядку.

> **Зауваження**: Оскільки цілий тип PHP є знаковим, деякі значення, отримані за допомогою цього методу, можуть перетворитися на негативні цілі числа на 32-бітових платформах. Для отримання строкового представлення беззнакового цілого можна скористатися шаблоном форматування %u функції [sprintf()](function.sprintf.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає компонент позначки часу Timestamp.

**Увага**

У 32-бітових системах цей метод може повертати негативне число. Хоча частини збільшення та позначки часу типу позначки часу BSON складаються з двох 32-розрядних значень без знака, PHP не може представити їх на 32-розрядних платформах.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [» Типи BSON: Timestamps](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps)
