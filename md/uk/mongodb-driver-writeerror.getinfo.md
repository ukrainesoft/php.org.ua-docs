Повертає документ метаданих для WriteError

-   [« MongoDBDriverWriteError::getIndex](mongodb-driver-writeerror.getindex.html)
    
-   [MongoDBDriverWriteError::getMessage »](mongodb-driver-writeerror.getmessage.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverWriteError](class.mongodb-driver-writeerror.html)
    
-   Повертає документ метаданих для WriteError
    

# MongoDBDriverWriteError::getInfo

(mongodb >=1.0.0)

MongoDBDriverWriteError::getInfo — Повертає документ метаданих для WriteError

### Опис

```methodsynopsis
final public MongoDB\Driver\WriteError::getInfo(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає документ метаданих для WriteError, або **`null`**, якщо метадані недоступні.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)