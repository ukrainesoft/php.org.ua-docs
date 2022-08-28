Повертає сервер, з яким пов'язаний курсор

-   [« MongoDB\\Driver\\CursorInterface::getId](mongodb-driver-cursorinterface.getid.html)
    
-   [MongoDB\\Driver\\CursorInterface::isDead »](mongodb-driver-cursorinterface.isdead.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.html)
    
-   Повертає сервер, з яким пов'язаний курсор
    

# MongoDBDriverCursorInterface::getServer

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::getServer — Повертає сервер, з яким пов'язаний курсор

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::getServer(): MongoDB\Driver\Server
```

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html) пов'язаний із курсором. Це той сервер, на якому запущено [MongoDB\\Driver\\Query](class.mongodb-driver-query.html) або [MongoDB\\Driver\\Command](class.mongodb-driver-command.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає [MongoDB\\Driver\\Server](class.mongodb-driver-server.html) пов'язаний із курсором.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::getServer()](mongodb-driver-cursor.getserver.html) - Повертає сервер, пов'язаний із курсором
-   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html)