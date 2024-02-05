---
navigation:
  - class.mongodb-bson-serializable.md: « MongoDB\\BSON\\Serializable
  - class.mongodb-bson-unserializable.md: MongoDB\\BSON\\Unserializable »
  - index.md: PHP Manual
  - class.mongodb-bson-serializable.md: MongoDB\\BSON\\Serializable
title: 'MongoDB\\BSON\\Serializable::bsonSerialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\BSON\\Serializable::bsonSerialize

(mongodb >=1.0.0)

MongoDB\\BSON\\Serializable::bsonSerialize — Надає масив або документ для серіалізації в BSON

### Опис

```methodsynopsis
abstract public MongoDB\BSON\Serializable::bsonSerialize(): array|stdClass|MongoDB\BSON\Document|MongoDB\BSON\PackedArray
```

Викликається під час серіалізації об'єкта BSON. Метод повинен повертати масив (array) або екземпляр одного із класів: [stdClass](class.stdclass.md) [MongoDB\\BSON\\Document](class.mongodb-bson-document.md), или[MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md)

Кореневі документи (наприклад, [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.md), передані в [MongoDB\\BSON\\fromPHP()](function.mongodb.bson-fromphp.md)) завжди будуть серіалізовані як документ BSON. Для значень полів асоціативні масиви та екземпляри [stdClass](class.stdclass.md) будуть серіалізовані у вигляді документа BSON, а послідовні масиви (наприклад, послідовні числові індекси, що починаються з ) будуть серіалізовані у вигляді масиву BSON.

Користувачам рекомендовано включати властивість \_id (наПриклад,[MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md), ініціалізований у конструкторі) при поверненні даних для кореневого документа BSON; інакше драйвер чи база даних повинні будуть згенерувати [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.md) при вставці чи злитті документа, відповідно.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array) або об'єкт одного із класів: [stdClass](class.stdclass.md) [MongoDB\\BSON\\Document](class.mongodb-bson-document.md), или[MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md), який буде серіалізовано як масив BSON або документ.

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.17.0 |  |
| Тип, що повертається, був змінений з array | об'єкт. Замість object тип, що повертається, тепер визначений як об'єкт класу [stdClass](class.stdclass.md). . Класи, які реалізують цей інтерфейс, повинні бути змінені, щоб більше не оголошувати тип object, що повертається. Оскільки тип, що повертається, попередньо оголошений, у PHP 8.1 або більше нових версіях видається попередження про старіння. |

На додаток до раніше описаних змін, драйвер також підтримує повернення екземплярів класів [MongoDB\\BSON\\Document](class.mongodb-bson-document.md) і [MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md). Будь ласка, зверніть увагу, що будь-які повернені екземпляри класу [MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md) автоматично перетворюються на об'єкти при збереженні як кореневих документів. Вони зберігаються як масивів, коли вказуються як значення вбудованого поля.

### Приклади

**Приклад #1**MongoDB\\BSON\\Serializable::bsonSerialize()**возвращение ассоциативного массива для корневого документа**

```php
<?php

class MyDocument implements MongoDB\BSON\Serializable
{
    private $id;

    function __construct()
    {
        $this->id = new MongoDB\BSON\ObjectId;
    }

    function bsonSerialize(): array
    {
        return ['_id' => $this->id, 'foo' => 'bar'];
    }
}

$bson = MongoDB\BSON\fromPHP(new MyDocument);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Висновок наведеного прикладу буде схожим на:

```
{ "_id" : { "$oid" : "56cccdcada14d8755a58c591" }, "foo" : "bar" }
```

**Приклад #2 Приклад использования метода**MongoDB\\BSON\\Serializable::bsonSerialize()**, що повертає асоціативний масив для кореневого документа**

```php
<?php

class MyArray implements MongoDB\BSON\Serializable
{
    function bsonSerialize(): array
    {
        return [1, 2, 3];
    }
}

$bson = MongoDB\BSON\fromPHP(new MyArray);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Результат виконання наведеного прикладу:

```
{ "0" : 1, "1" : 2, "2" : 3 }
```

**Приклад #3**MongoDB\\BSON\\Serializable::bsonSerialize()**возвращение ассоциативного массива для поля документа**

```php
<?php

class MyDocument implements MongoDB\BSON\Serializable
{
    function bsonSerialize(): array
    {
        return ['foo' => 'bar'];
    }
}

$value = ['document' => new MyDocument];
$bson = MongoDB\BSON\fromPHP($value);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Результат виконання наведеного прикладу:

```
{ "document" : { "foo" : "bar" } }
```

**Приклад #4**MongoDB\\BSON\\Serializable::bsonSerialize()**возвращение последовательного массива для поля документа**

```php
<?php

class MyArray implements MongoDB\BSON\Serializable
{
    function bsonSerialize(): array
    {
        return [1, 2, 3];
    }
}

$value = ['array' => new MyArray];
$bson = MongoDB\BSON\fromPHP($value);
echo MongoDB\BSON\toJSON($bson), "\n";

?>
```

Результат виконання наведеного прикладу:

```
{ "array" : [ 1, 2, 3 ] }
```

### Дивіться також

-   [MongoDB\\BSON\\Unserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.md) \- Створює об'єкт із масиву BSON або документа
-   [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md)
-   [Постійні дані](mongodb.persistence.md)
