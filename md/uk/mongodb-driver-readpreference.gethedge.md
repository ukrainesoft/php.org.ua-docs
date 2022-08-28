Повертає опцію "hedge" із ReadPreference

-   [« MongoDB\\Driver\\ReadPreference::\_\_construct](mongodb-driver-readpreference.construct.html)
    
-   [MongoDB\\Driver\\ReadPreference::getMaxStalenessSeconds »](mongodb-driver-readpreference.getmaxstalenessseconds.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [» документация по Read Preference](https://www.mongodb.com/docs/manual/core/read-preference/)