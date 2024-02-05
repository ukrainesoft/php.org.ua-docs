---
navigation:
  - mongodb-driver-cursor.construct.md: '« MongoDB\\Driver\\Cursor::\_\_construct'
  - mongodb-driver-cursor.getid.md: 'MongoDB\\Driver\\Cursor::getId »'
  - index.md: PHP Manual
  - class.mongodb-driver-cursor.md: MongoDB\\Driver\\Cursor
title: 'MongoDB\\Driver\\Cursor::current'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Cursor::current

(mongodb >=1.9.0)

MongoDB\\Driver\\Cursor::current — Повертає поточний елемент

### Опис

```methodsynopsis
public MongoDB\Driver\Cursor::current(): array|object|null
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний документ у вигляді масиву або об'єкта залежно від налаштувань курсору. Якщо ітерація не була розпочата, або поточна позиція не коректна, буде повернено **`null`**

### Дивіться також

-   [Iterator::current()](iterator.current.md) \- Повернення поточного елемента
