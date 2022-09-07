---
navigation:
  - mongodb-driver-cursor.next.md: '« MongoDBDriverCursor::next'
  - mongodb-driver-cursor.settypemap.md: 'MongoDBDriverCursor::setTypeMap »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDBDriverCursor
title: 'MongoDBDriverCursor::rewind'
---
# MongoDBDriverCursor::rewind

(mongodb >=1.9.0)

MongoDBDriverCursor::rewind — Переміщує курсор до першого результату

### Опис

```methodsynopsis
public MongoDB\Driver\Cursor::rewind(): void
```

Якщо курсор просунувся далі своєї першої позиції, його перемістити до першого результату не вийде.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`null`**

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Кидає виняток [MongoDBDriverExceptionLogicException](class.mongodb-driver-exception-logicexception.md) якщо метод був викликаний після просування курсору далі за свою першу позицію.

### Дивіться також

-   [Iterator::rewind()](iterator.rewind.md) – Повертає ітератор на перший елемент
