Повернути всі результати для даного курсору у вигляді масиву

-   [« MongoDB\\Driver\\CursorInterface::setTypeMap](mongodb-driver-cursorinterface.settypemap.html)
    
-   [MongoDB\\Driver\\Server »](class.mongodb-driver-server.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.html)
    
-   Повернути всі результати для даного курсору у вигляді масиву
    

# MongoDBDriverCursorInterface::toArray

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::toArray — Повернути всі результати для даного курсору у вигляді масиву

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::toArray(): array
```

Ітерує курсор та повертає результати у вигляді масиву. Для контролю десеріалізації типи PHP можна використовувати [MongoDB\\Driver\\CursorInterface::setTypeMap()](mongodb-driver-cursorinterface.settypemap.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить усі результати курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::toArray()](mongodb-driver-cursor.toarray.html) - Повертає масив, що містить усі результати курсору
-   [MongoDB\\Driver\\CursorInterface::setTypeMap()](mongodb-driver-cursorinterface.settypemap.html) - Задати порівняння типів для десеріалізації BSON