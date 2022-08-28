Повертає ідентифікатор курсору

-   [« MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.html)
    
-   [MongoDB\\Driver\\CursorInterface::getServer »](mongodb-driver-cursorinterface.getserver.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.html)
    
-   Повертає ідентифікатор курсору
    

# MongoDBDriverCursorInterface::getId

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::getId — Повертає ідентифікатор курсору

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getId(): MongoDB\Driver\CursorId
```

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html) пов'язаний із курсором. Кожен курсор має унікальний ідентифікатор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html) для курсору.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::getId()](mongodb-driver-cursor.getid.html) - Повертає ідентифікатор для курсору
-   [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html)
-   [MongoDB\\Driver\\CursorId::\_\_toString()](mongodb-driver-cursorid.tostring.html) - Строкове подання ідентифікатора курсору