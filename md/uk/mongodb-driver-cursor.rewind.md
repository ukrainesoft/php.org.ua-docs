---
navigation:
  - mongodb-driver-cursor.next.md: '« MongoDB\\Driver\\Cursor::next'
  - mongodb-driver-cursor.settypemap.md: 'MongoDB\\Driver\\Cursor::setTypeMap »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDB\\Driver\\Cursor
title: 'MongoDB\\Driver\\Cursor::rewind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Cursor::rewind

(mongodb >=1.9.0)

MongoDB\\Driver\\Cursor::rewind — Переміщує курсор до першого результату

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   При невдалому з'єднанні з сервером (крім помилок аутентифікації) кидає виняток[MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.md)
-   У разі невдалої аутентифікації кидає виняток[MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.md)
-   Кидає виняток [MongoDB\\Driver\\Exception\\LogicException](class.mongodb-driver-exception-logicexception.md)якщо метод був викликаний після просування курсору далі за свою першу позицію.

### Дивіться також

-   [Iterator::rewind()](iterator.rewind.md)– Повертає ітератор на перший елемент
