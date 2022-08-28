Задати порівняння типів для десеріалізації BSON

-   [« MongoDB\\Driver\\CursorInterface::isDead](mongodb-driver-cursorinterface.isdead.html)
    
-   [MongoDB\\Driver\\CursorInterface::toArray »](mongodb-driver-cursorinterface.toarray.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.html)
    
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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Cursor::setTypeMap()](mongodb-driver-cursor.settypemap.html) - Встановлює карту типу для десеріалізації BSON
-   [Постоянные данные](mongodb.persistence.html)