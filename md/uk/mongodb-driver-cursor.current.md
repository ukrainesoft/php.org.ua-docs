---
navigation:
  - mongodb-driver-cursor.construct.md: '« MongoDBDriverCursor::construct'
  - mongodb-driver-cursor.getid.md: 'MongoDBDriverCursor::getId »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDBDriverCursor
title: 'MongoDBDriverCursor::current'
---
# MongoDBDriverCursor::current

(mongodb >=1.9.0)

MongoDBDriverCursor::current — Повертає поточний елемент

### Опис

```methodsynopsis
public MongoDB\Driver\Cursor::current(): array|object|null
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний документ у вигляді масиву або об'єкта залежно від налаштувань курсору. Якщо ітерація не була розпочата, або поточна позиція не коректна, буде повернено **`null`**

### Дивіться також

-   [Iterator::current()](iterator.current.md) - Повернення поточного елемента
