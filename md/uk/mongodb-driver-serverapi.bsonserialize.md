Повертає об'єкт для серіалізації BSON

-   [« MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.html)
    
-   [MongoDB\\Driver\\ServerApi::\_\_construct »](mongodb-driver-serverapi.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.html)
    
-   Повертає об'єкт для серіалізації BSON
    

# MongoDBDriverServerApi::bsonSerialize

(mongodb >=1.10.0)

MongoDBDriverServerApi::bsonSerialize — Повертає об'єкт для серіалізації BSON

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::bsonSerialize(): object
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт для серіалізації ServerApi як BSON.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) - Надає масив або документ для серіалізації у BSON