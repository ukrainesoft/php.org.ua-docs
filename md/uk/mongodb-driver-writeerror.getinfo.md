Повертає документ метаданих для WriteError

-   [« MongoDB\\Driver\\WriteError::getIndex](mongodb-driver-writeerror.getindex.html)
    
-   [MongoDB\\Driver\\WriteError::getMessage »](mongodb-driver-writeerror.getmessage.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)