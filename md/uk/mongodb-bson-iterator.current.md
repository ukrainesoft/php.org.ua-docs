---
navigation:
  - mongodb-bson-iterator.construct.md: '« MongoDB\\BSON\\Iterator::\_\_construct'
  - mongodb-bson-iterator.key.md: 'MongoDB\\BSON\\Iterator::key »'
  - index.md: PHP Manual
  - class.mongodb-bson-iterator.md: MongoDB\\BSON\\Iterator
title: 'MongoDB\\BSON\\Iterator::current'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Iterator::current

(mongodb >=1.16.0)

MongoDB\\BSON\\Iterator::current — Повертає поточний елемент

### Опис

```methodsynopsis
public MongoDB\BSON\Iterator::current(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає значення поточного елемента.

> **Зауваження**: Якщо в структурі BSON зустрічається значення, закодоване як 64-бітове ціле число, то значенням методу, що повертається, буде екземпляр [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.md)

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Викидає виняток[MongoDB\\Driver\\Exception\\LogicException](class.mongodb-driver-exception-logicexception.md)якщо ітератор не є коректним.

### Дивіться також

-   [Iterator::current()](iterator.current.md) \- Повернення поточного елемента
