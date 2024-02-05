---
navigation:
  - mongodb-bson-iterator.current.md: '« MongoDB\\BSON\\Iterator::current'
  - mongodb-bson-iterator.next.md: 'MongoDB\\BSON\\Iterator::next »'
  - index.md: PHP Manual
  - class.mongodb-bson-iterator.md: MongoDB\\BSON\\Iterator
title: 'MongoDB\\BSON\\Iterator::key'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Iterator::key

(mongodb >=1.16.0)

MongoDB\\BSON\\Iterator::key — Повертає ключ поточного елемента

### Опис

```methodsynopsis
public MongoDB\BSON\Iterator::key(): string|int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ключ поточного елемента. При ітерації документа BSON ключем завжди буде рядок (string). При ітерації масиву BSON ключем буде ціле число (int).

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток [MongoDB\\Driver\\Exception\\LogicException](class.mongodb-driver-exception-logicexception.md)якщо ітератор не є коректним.

### Дивіться також

-   [Iterator::key()](iterator.key.md) \- Повертає ключ поточного елемента
