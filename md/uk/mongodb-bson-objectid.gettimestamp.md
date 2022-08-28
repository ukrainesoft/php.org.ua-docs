Повертає позначку часу ObjectId

-   [« MongoDB\\BSON\\ObjectId::\_\_construct](mongodb-bson-objectid.construct.html)
    
-   [MongoDB\\BSON\\ObjectId::jsonSerialize »](mongodb-bson-objectid.jsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html)
    
-   Повертає позначку часу ObjectId
    

# MongoDBBSONObjectId::getTimestamp

(mongodb >=1.2.0)

MongoDBBSONObjectId::getTimestamp — Повертає позначку часу ObjectId

### Опис

```methodsynopsis
final public MongoDB\BSON\ObjectId::getTimestamp(): int
```

Компонент мітки часу в ObjectId – це його найбільш значущі 32 біти, які позначають кількість секунд від початку епохи Unix. Це значення читається як 32-розрядне ціле число без знака з порядком байтів у старшому порядку.

> **Зауваження**: Оскільки цілий тип PHP є знаковим, деякі значення, отримані за допомогою цього методу, можуть перетворитися на негативні цілі числа на 32-бітових платформах. Для отримання рядкового представлення беззнакового цілого можна скористатися шаблоном форматування %u функції [sprintf()](function.sprintf.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає позначку часу ObjectId.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Приклади

**Приклад #1 Приклад використання **MongoDBBSONObjectId::getTimestamp()****

```php
<?php

var_dump((new MongoDB\BSON\ObjectId())->getTimestamp());

var_dump((new MongoDB\BSON\ObjectId('0000002a0000000000000000'))->getTimestamp());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
integer(1484854719)
integer(42)
```

### Дивіться також

-   [» Справка по ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)
-   [» Типы BSON: ObjectId](https://www.mongodb.com/docs/manual/reference/bson-types/#objectid)