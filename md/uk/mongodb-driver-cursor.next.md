---
navigation:
  - mongodb-driver-cursor.key.md: '« MongoDB\\Driver\\Cursor::key'
  - mongodb-driver-cursor.rewind.md: 'MongoDB\\Driver\\Cursor::rewind »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDB\\Driver\\Cursor
title: 'MongoDB\\Driver\\Cursor::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Cursor::next

(mongodb >=1.9.0)

MongoDB\\Driver\\Cursor::next — Переміщує курсор на наступний результат

### Опис

```methodsynopsis
public MongoDB\Driver\Cursor::next(): void
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Зсув поточної позиції до наступного результату в курсорі.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)

### Дивіться також

-   [Iterator::next()](iterator.next.md) \- Переходить до наступного елементу
