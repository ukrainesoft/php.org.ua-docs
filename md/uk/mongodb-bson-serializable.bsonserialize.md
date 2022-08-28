Надає масив або документ для серіалізації в BSON

-   [« MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html)
    
-   [MongoDB\\BSON\\Unserializable »](class.mongodb-bson-unserializable.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html)
    
-   Надає масив або документ для серіалізації в BSON
    

# MongoDBBSONSerializable::bsonSerialize

(mongodb >=1.0.0)

MongoDBBSONSerializable::bsonSerialize — Надає масив або документ для серіалізації в BSON

### Опис

```methodsynopsis
abstract public MongoDB\BSON\Serializable::bsonSerialize(): array|object
```

Викликається під час серіалізації об'єкта BSON. Метод повинен повертати array або **stdClass**

Кореневі документи (наприклад, [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html), передані в [MongoDB\\BSON\\fromPHP()](function.mongodb.bson-fromphp.html)) завжди будуть серіалізовані як документ BSON. Для значень полів асоціативні масиви та екземпляри **stdClass** будуть серіалізовані у вигляді документа BSON, а послідовні масиви (наприклад, послідовні числові індекси, що починаються з `0`) будуть серіалізовані у вигляді масиву BSON.

Користувачам рекомендується включати властивість id (наприклад, [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html), ініціалізований у вашому конструкторі) при поверненні даних для кореневого документа BSON; в іншому випадку драйвер або база даних повинні будуть згенерувати [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html) при вставці чи злитті документа, відповідно.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

array або **stdClass** для серіалізації у вигляді масиву чи документа BSON.

### Приклади

**Приклад #1 **MongoDBBSONSerializable::bsonSerialize()** повернення асоціативного масиву для кореневого документа**

```php
<?php

class MyDocument implements MongoDB\BSON\Serializable
{
    private $id;

    function __construct()
    {
        $this->id = new MongoDB\BSON\ObjectId;
    }

    function bsonSerialize(): array
    {
        return ['_id' => $this->id, 'foo' => 'bar'];
    }
}

$bson = MongoDB\BSON\fromPHP(new MyDocument);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
{ "_id" : { "$oid" : "56cccdcada14d8755a58c591" }, "foo" : "bar" }
```

**Приклад #2 **MongoDBBSONSerializable::bsonSerialize()** повернення послідовного масиву для кореневого документа**

```php
<?php

class MyArray implements MongoDB\BSON\Serializable
{
    function bsonSerialize(): array
    {
        return [1, 2, 3];
    }
}

$bson = MongoDB\BSON\fromPHP(new MyArray);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Результат виконання цього прикладу:

```
{ "0" : 1, "1" : 2, "2" : 3 }
```

**Приклад #3 **MongoDBBSONSerializable::bsonSerialize()** повернення асоціативного масиву для поля документа**

```php
<?php

class MyDocument implements MongoDB\BSON\Serializable
{
    function bsonSerialize(): array
    {
        return ['foo' => 'bar'];
    }
}

$value = ['document' => new MyDocument];
$bson = MongoDB\BSON\fromPHP($value);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Результат виконання цього прикладу:

```
{ "document" : { "foo" : "bar" } }
```

**Приклад #4 **MongoDBBSONSerializable::bsonSerialize()** повернення послідовного масиву для поля документа**

```php
<?php

class MyArray implements MongoDB\BSON\Serializable
{
    function bsonSerialize(): array
    {
        return [1, 2, 3];
    }
}

$value = ['array' => new MyArray];
$bson = MongoDB\BSON\fromPHP($value);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Результат виконання цього прикладу:

```
{ "array" : [ 1, 2, 3 ] }
```

### Дивіться також

-   [MongoDB\\BSON\\Unserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.html) - Створює об'єкт із масиву BSON або документа
-   [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.html)
-   [Постоянные данные](mongodb.persistence.html)