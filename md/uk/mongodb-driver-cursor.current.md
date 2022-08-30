Повертає поточний елемент

-   [« MongoDBDriverCursor::construct](mongodb-driver-cursor.construct.html)
    
-   [MongoDBDriverCursor::getId »](mongodb-driver-cursor.getid.html)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverCursor](class.mongodb-driver-cursor.html)
    
-   Повертає поточний елемент
    

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