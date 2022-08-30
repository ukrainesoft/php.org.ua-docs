Повертає опцію "hedge" із ReadPreference

-   [« MongoDBDriverReadPreference::construct](mongodb-driver-readpreference.construct.html)
    
-   [MongoDBDriverReadPreference::getMaxStalenessSeconds »](mongodb-driver-readpreference.getmaxstalenessseconds.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html)
    
-   Повертає опцію "hedge" із ReadPreference
    

# MongoDBDriverReadPreference::getHedge

(mongodb >=1.8.0)

MongoDBDriverReadPreference::getHedge — Повертає опцію "hedge" із ReadPreference

### Опис

```methodsynopsis
final public MongoDB\Driver\ReadPreference::getHedge(): ?object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає опцію "hedge" із ReadPreference.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [» документация по Read Preference](https://www.mongodb.com/docs/manual/core/read-preference/)