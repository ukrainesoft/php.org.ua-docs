---
navigation:
  - mongodb-driver-cursor.key.html: '« MongoDBDriverCursor::key'
  - mongodb-driver-cursor.rewind.html: 'MongoDBDriverCursor::rewind »'
  - index.html: PHP Manual
  - class.mongodb-driver-cursor.html: MongoDBDriverCursor
title: 'MongoDBDriverCursor::next'
---
# MongoDBDriverCursor::next

(mongodb >=1.9.0)

MongoDBDriverCursor::next — Переміщує курсор на наступний результат

### Опис

```methodsynopsis
public MongoDB\Driver\Cursor::next(): void
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Зсув поточної позиції до наступного результату в курсорі.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)

### Дивіться також

-   [Iterator::next()](iterator.next.md) - Переходить до наступного елементу
