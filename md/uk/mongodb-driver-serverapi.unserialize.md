Десеріалізує ServerApi

-   [« MongoDB\\Driver\\ServerApi::serialize](mongodb-driver-serverapi.serialize.html)
    
-   [MongoDB\\Driver\\WriteConcern »](class.mongodb-driver-writeconcern.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.html)
    
-   Десеріалізує ServerApi
    

# MongoDBDriverServerApi::unserialize

(mongodb >=1.10.0)

MongoDBDriverServerApi::unserialize — Десеріалізує ServerApi

### Опис

```methodsynopsis
final public MongoDB\Driver\ServerApi::unserialize(string $serialized): void
```

### Список параметрів

`serialized`

Серіалізований [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Викидає [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)якщо властивості не можуть бути десеріалізовані (наприклад, `serialized` було некоректно сформовано).
-   Викидає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)якщо властивості некоректні (наприклад, відсутні поля або містяться неприпустимі значення).

### Дивіться також

-   [MongoDB\\Driver\\ServerApi::serialize()](mongodb-driver-serverapi.serialize.html) - Серіалізує ServerApi
-   [unserialize()](function.unserialize.html) - Створює PHP-значення зі збереженого уявлення
-   [Сериализация объектов](language.oop5.serialization.html)