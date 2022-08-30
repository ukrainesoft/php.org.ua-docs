Повертає сервер, з яким пов'язаний курсор

-   [« MongoDBDriverCursorInterface::getId](mongodb-driver-cursorinterface.getid.html)
    
-   [MongoDBDriverCursorInterface::isDead »](mongodb-driver-cursorinterface.isdead.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverCursorInterface](class.mongodb-driver-cursorinterface.html)
    
-   Повертає сервер, з яким пов'язаний курсор
    

# MongoDBDriverCursorInterface::getServer

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::getServer — Повертає сервер, з яким пов'язаний курсор

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html) пов'язаний із курсором. Це той сервер, на якому запущено [MongoDBDriverQuery](class.mongodb-driver-query.html) або [MongoDBDriverCommand](class.mongodb-driver-command.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDBDriverServer](class.mongodb-driver-server.html) пов'язаний із курсором.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverCursor::getServer()](mongodb-driver-cursor.getserver.html) - Повертає сервер, пов'язаний із курсором
-   [MongoDBDriverServer](class.mongodb-driver-server.html)