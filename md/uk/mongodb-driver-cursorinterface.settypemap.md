Задати порівняння типів для десеріалізації BSON

-   [« MongoDBDriverCursorInterface::isDead](mongodb-driver-cursorinterface.isdead.html)
    
-   [MongoDBDriverCursorInterface::toArray »](mongodb-driver-cursorinterface.toarray.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverCursorInterface](class.mongodb-driver-cursorinterface.html)
    
-   Задати порівняння типів для десеріалізації BSON
    

# MongoDBDriverCursorInterface::setTypeMap

(mongodb >=1.6.0)

MongoDBDriverCursorInterface::setTypeMap — Задати порівняння типів для десеріалізації BSON

### Опис

```methodsynopsis
abstract public MongoDB\Driver\CursorInterface::setTypeMap(array $typemap): void
```

Задати [сопоставление типов](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps) для використання при десеріалізації результатів BSON значення PHP.

### Список параметрів

`typeMap` (array)

[Конфигурация карты типов](mongodb.persistence.deserialization.html#mongodb.persistence.typemaps)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverCursor::setTypeMap()](mongodb-driver-cursor.settypemap.html) - Встановлює карту типу для десеріалізації BSON
-   [Постійні дані](mongodb.persistence.html)