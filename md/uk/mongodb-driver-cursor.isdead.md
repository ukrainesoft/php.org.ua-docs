---
navigation:
  - mongodb-driver-cursor.getserver.md: '« MongoDBDriverCursor::getServer'
  - mongodb-driver-cursor.key.md: 'MongoDBDriverCursor::key »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDBDriverCursor
title: 'MongoDBDriverCursor::isDead'
---
# MongoDBDriverCursor::isDead

(mongodb >=1.0.0)

MongoDBDriverCursor::isDead — Перевіряє, чи курсор вичерпано, чи може містити додаткові результати.

### Опис

```methodsynopsis
final public MongoDB\Driver\Cursor::isDead(): bool
```

Перевіряє, чи немає курсора додаткових результатів. Цей метод аналогічний методу [» cursor.isExhausted()](https://www.mongodb.com/docs/manual/reference/method/cursor.isExhausted/) в оболонці MongoDB і насамперед корисний при виконанні ітерації [» хвостових курсорів](https://www.mongodb.com/docs/manual/core/tailable-cursors/)

Курсор не має додаткових результатів і вважається "мертвим", якщо виконується одна з наступних умов:

-   Поточний пакет повністю повторений *і* ідентифікатор курсору дорівнює нулю (тобто [» getMore](https://www.mongodb.com/docs/manual/reference/command/getMore/) не може бути виконаний).
-   Сталася помилка під час ітерації курсору.
-   Курсор досяг своєї встановленої межі.

Навмисно не завжди можна визначити, чи курсор має додаткові результати. Випадки, коли курсор *може* мати більше доступних даних, такі:

-   У поточному пакеті є додаткові документи, які буферизуються за клієнта. Ітерація витягне документ із локального буфера.
-   У пакеті немає додаткових документів (тобто локального буфера), але ідентифікатор курсору не дорівнює нулю. Ітерація вимагатиме більше документів із сервера за допомогою операції [» getMore](https://www.mongodb.com/docs/manual/reference/command/getMore/)яка може повертати або не повертати додаткові результати та/або вказувати, що курсор був закритий на сервері, повертаючи нуль для його ідентифікатора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо курсор не містить жодних додаткових результатів та **`false`** в іншому випадку.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Приклади

**Приклад #1 Приклад використання **MongoDBDriverCursor::isDead()****

```php
<?php

$manager = new MongoDB\Driver\Manager("mongodb://localhost:27017");
$query = new MongoDB\Driver\Query([]);

$bulk = new MongoDB\Driver\BulkWrite;
$bulk->insert(['x' => 1]);
$bulk->insert(['x' => 2]);
$bulk->insert(['x' => 3]);
$manager->executeBulkWrite('db.collection', $bulk);

$cursor = $manager->executeQuery('db.collection', $query);

$iterator = new IteratorIterator($cursor);

$iterator->rewind();
var_dump($cursor->isDead());

$iterator->next();
var_dump($cursor->isDead());

$iterator->next();
var_dump($cursor->isDead());

$iterator->next();
var_dump($cursor->isDead());

?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [» Хвостові курсори](https://www.mongodb.com/docs/manual/core/tailable-cursors/) у посібнику MongoDB
-   [» cursor.isExhausted()](https://www.mongodb.com/docs/manual/reference/method/cursor.isExhausted/) у посібнику MongoDB
