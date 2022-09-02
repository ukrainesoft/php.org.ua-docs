---
navigation:
  - mongodb-bson-timestamp.construct.md: '« MongoDBBSONTimestamp::construct'
  - mongodb-bson-timestamp.gettimestamp.md: 'MongoDBBSONTimestamp::getTimestamp »'
  - index.md: PHP Manual
  - class.mongodb-bson-timestamp.md: MongoDBBSONTimestamp
title: 'MongoDBBSONTimestamp::getIncrement'
---
# MongoDBBSONTimestamp::getIncrement

(mongodb >=1.3.0)

MongoDBBSONTimestamp::getIncrement — Повертає компонент збільшення Timestamp

### Опис

```methodsynopsis
final public MongoDB\BSON\Timestamp::getIncrement(): int
```

Компонент збільшення Timestamp - це його молодші 32 біти, які позначають порядковий номер збільшення для операцій протягом цієї секунди. Це значення читається як 32-розрядне ціле число без знака з порядком байтів у старшому порядку.

> **Зауваження**: Оскільки цілий тип PHP є знаковим, деякі значення, отримані за допомогою цього методу, можуть перетворитися на негативні цілі числа на 32-бітових платформах. Для отримання рядкового представлення беззнакового цілого можна скористатися шаблоном форматування %u функції [sprintf()](function.sprintf.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає компонент збільшення Timestamp.

**Увага**

У 32-бітових системах цей метод може повертати негативне число. Хоча частини збільшення та позначки часу типу позначки часу BSON складаються з двох 32-розрядних значень без знака, PHP не може представити їх на 32-розрядних платформах.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [» Типи BSON: Timestamps](https://www.mongodb.com/docs/manual/reference/bson-types/#timestamps)
