Десеріалізація з BSON

-   [« Сериализация в BSON](mongodb.persistence.serialization.md)
    
-   [Безпека »](mongodb.security.md)
    
-   [PHP Manual](index.md)
    
-   [Постійні дані](mongodb.persistence.md)
    
-   Десеріалізація з BSON
    

## Десеріалізація з BSON

**Увага**

Документи BSON технічно можуть містити ключі, що повторюються, оскільки документи зберігаються у вигляді списку пар ключ-значення; однак програмам слід утримуватися від створення документів з дублікатами ключів, оскільки поведінка сервера та драйвера може бути невизначеною. Оскільки об'єкти та масиви PHP не можуть мати ключів, що повторюються, дані також можуть бути втрачені при декодуванні документа BSON з повторюваними ключами.

Застарілий модуль `mongo` десеріалізував як документи, так і масиви BSON як масиви PHP. Хоча з PHP масивами зручно працювати, така поведінка була проблематичною, оскільки різні типи BSON можуть десеріалізуватися до одного і того ж значення PHP (наприклад, `{"0": "foo"}` і `["foo"]`) і неможливо буде вивести оригінальний тип BSON. За промовчанням поточний драйвер вирішує цю проблему, забезпечуючи перетворення масивів та документів BSON на масиви та об'єкти PHP відповідно.

Для складових типів існує три типи даних:

root

відноситься *тільки* до документа верхнього рівня BSON

document

відноситься *тільки* до вбудованих документів BSON

array

відноситься до масивів BSON

Крім трьох групових типів, можна налаштувати певні поля в документі для порівняння з типами даних, вказаними нижче. Як приклад, наступна карта типів дозволяє зіставити кожен вбудований документ у масиві `"addresses"` з класом **Address** *а* кожне поле `"city"` у цих документах із вбудованою адресою з класом **City**

'fieldPaths' => 'addresses.$' => 'MyProjectAddress', 'addresses.$.city' => 'MyProjectCity',

Кожен із цих трьох типів даних, а також зіставлення для конкретних полів можуть бути зіставлені з різними типами PHP. Можливі значення зіставлення:

*не вказано* або NULL (за замовчуванням)

-   Масив BSON буде десеріалізований, як PHP array.
    
-   Документ BSON (кореневий або впроваджений) без якості pclass [](#fnidmongodb.pclass)стає об'єктом PHP **stdClass**, причому кожен ключ документа BSON встановлюється як відкрита властивість **stdClass**
    
-   Документ BSON (кореневий або вбудований) з властивістю pclass [](#fnidmongodb.pclass)стає об'єктом PHP імені класу, як це визначено властивістю pclass.
    
    Якщо цей клас реалізує інтерфейс M[MongoDBBSONPersistable](class.mongodb-bson-persistable.html), то властивості документа BSON, включаючи властивість pclass, відправляються у вигляді асоціативного масиву у функцію [MongoDBBSONUnserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.html) для ініціалізації властивостей об'єкта
    
    Якщо названий клас не існує або не реалізує інтерфейс [MongoDBBSONPersistable](class.mongodb-bson-persistable.html), використовуватиметься **stdClass**, і кожен ключ документа BSON (включаючи pclass) буде встановлено як відкриту властивість **stdClass**
    
    Функціональність pclass залежить від того, чи є властивістю частиною вилученого документа MongoDB. Якщо ви використовуєте [проекцію](mongodb-driver-query.construct.html#mongodb-driver-query.construct-queryOptions) при запиті документів, потрібно включити поле pclass у проекцію, щоб ця функція працювала.
    

`"array"`

Перетворює масив BSON або документ BSON на масив PHP. Не буде спеціальної обробки властивості pclass [](#fnidmongodb.pclass), але його можна встановити, як елемент у масиві, що повертається, якщо він був присутній в документі BSON.

`"object"` або `"stdClass"`

Перетворює масив BSON або документ BSON на об'єкт **stdClass**. Не буде спеціальної обробки властивості pclass [](#fnidmongodb.pclass), але вона може бути встановлена ​​як відкрита властивість у об'єкті, що повертається, якщо вона була присутня в документі BSON.

будь-який інший рядок

Визначає назву класу, який повинен десеріалізувати масив BSON або об'єкт BSON. Для об'єктів BSON, які містять властивості pclass, цей клас матиме пріоритет.

Якщо названий клас не існує, не є конкретним (тобто абстрактним або інтерфейсом) або не реалізує [MongoDBBSONUnserializable](class.mongodb-bson-unserializable.html), то видається виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

Якщо об'єкт BSON має властивість pclass, і цей клас існує та реалізує [MongoDBBSONPersistable](class.mongodb-bson-persistable.html), він замінить клас, представлений у карті типів.

Властивості документа BSON, *включаючи* властивість pclass, якщо воно існує, буде відправлено у вигляді асоціативного масиву в функцію [MongoDBBSONUnserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.html) для ініціалізації властивостей об'єкта

## TypeMaps

TypeMaps можна встановити за допомогою методу [MongoDBDriverCursor::setTypeMap()](mongodb-driver-cursor.settypemap.html) для об'єкту [MongoDBDriverCursor](class.mongodb-driver-cursor.html) або аргументу `$typeMap` в [MongoDBBSONtoPHP()](function.mongodb.bson-tophp.html). Кожен із трьох класів (*root* *document*, і *array*) може бути заданий індивідуально, на додаток до типів полів.

Якщо значення на карті дорівнює NULL, це означає те саме, що і значення *за замовчуванням* для цього елемента.

## Приклади

У цих прикладах використовуються такі класи:

MyClass

Котрий *не* реалізує інтерфейс

YourClass

який реалізує [MongoDBBSONUnserializable](class.mongodb-bson-unserializable.html)

OurClass

який реалізує [MongoDBBSONPersistable](class.mongodb-bson-persistable.html)

TheirClass

який розширює OurClass

Метод [MongoDBBSONUnserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.html) класу YourClass, OurClass, OurClass виконує ітерацію за масивом та встановлює властивості без змін. Він *також* встановлює для якості `$unserialized` значення `true`

```php
<?php

function bsonUnserialize( array $map )
{
    foreach ( $map as $k => $value )
    {
        $this->$k = $value;
    }
    $this->unserialized = true;
}
```

typemap: (усі значення за замовчуванням) / {"foo": "yes", "bar": false} -> stdClass { $foo => 'yes', $bar => false }

{ "foo": "no", "array": } -> stdClass { $foo => 'no', $array =>

{ "foo": "no", "obj" : { "embedded" : 3.14 } } -> stdClass { $foo => 'no', $obj => stdClass { $embedded => 3.14 } }

{ "foo": "yes", "pclass": "MyClass" } -> stdClass { $foo => 'yes', $pclass => 'MyClass' }

{ "foo": "yes", "pclass": { "$type" : "80", "$binary" : "MyClass" } } -> stdClass { $foo => 'yes', $pclass => Binary(0x80, 'MyClass') }

{ "foo": "yes", "pclass": { "$type" : "80", "$binary" : "YourClass") } -> stdClass { $foo => 'yes', $pclass => Binary(0x80, 'YourClass') }

{ "foo": "yes", "pclass": { "$type" : "80", "$binary" : "OurClass") } -> OurClass { $foo => 'yes', $pclass => Binary(0x80, 'OurClass'), $unserialized => true }

{ "foo": "yes", "pclass": { "$type" : "44", "$binary" : "YourClass") } -> stdClass { $foo => 'yes', $pclass => Binary(0x44, 'YourClass') }

typemap: "root" => "MissingClass" / { "foo": "yes" } -> MongoDBDriverExceptionInvalidArgumentException("MissingClass does not exist")

typemap: "root" => "MyClass" / { "foo": "yes", "pclass" : { "$type": "80", "$binary": "MyClass" } } -> MongoDBDriverExceptionInvalidArgumentException("MyClass не може реалізувати Unserializable interface")

typemap: "root" => "MongoDBBSONUnserializable" / { "foo": "yes" } -> MongoDBDriverExceptionInvalidArgumentException("Unserializable is not a concrete class")

typemap: "root" => "YourClass" / { "foo": "yes", "pclass" : { "$type": "80", "$binary": "MongoDBBSONUnserializable" } } -> YourClass { $foo => "yes", $pclass => Binary(0x80, "MongoDBBSONUnserializable"), $unserialized => true }

typemap: "root" => "YourClass" / { "foo": "yes", "pclass" : { "$type": "80", "$binary": "MyClass" } } -> YourClass { $foo => "yes", $pclass => Binary(0x80, "MyClass"), $unserialized => true }

typemap: "root" => "YourClass" / { "foo": "yes", "pclass" : { "$type": "80", "$binary": "OurClass" } } -> OurClass { $foo => "yes", $pclass => Binary(0x80, "OurClass"), $unserialized => true }

typemap: "root" => "YourClass" / { "foo": "yes", "pclass" : { "$type": "80", "$binary": "TheirClass" } } -> TheirClass { $foo => "yes", $pclass => Binary(0x80, "TheirClass"), $unserialized => true }

typemap: "root" => "OurClass" / { foo: "yes", "pclass" : { "$type": "80", "$binary": "TheirClass" } } -> TheirClass { $foo => "yes", $pclass => Binary(0x80, "TheirClass"), $unserialized => true }

typemap: 'root' => 'YourClass' / { foo: "yes", "pclass" : { "$type": "80", "$binary": "YourClass" } } -> YourClass { $foo => 'yes', $pclass => Binary(0x80, 'YourClass'), $unserialized => true }

typemap: 'root' => 'array', 'document' => 'array' / {"foo": "yes", "bar": false} -> "foo" => "yes", "bar" => false

{ "foo": "no", "array": } -> "foo" => "no", "array" =>

{ "foo": "no", "obj" : { "embedded" : 3.14 } } -> "foo" => "no", "obj" => "embedded => 3.14

{ "foo": "yes", "pclass": "MyClass" } -> "foo" => "yes", "pclass" => "MyClass"

{ "foo": "yes", "pclass" : { "$type": "80", "$binary": "MyClass" } } -> "foo" => "yes", "pclass" => Binary(0x80, "MyClass")

{ "foo": "yes", "pclass" : { "$type": "80", "$binary": "OurClass" } } -> "foo" => "yes", "pclass" => Binary(0x80, "OurClass")

typemap: 'root' => 'object', 'document' => 'object' / { "foo": "yes", "pclass": { "$type": "80", "$binary": "MyClass" } } -> stdClass { $foo => "yes", "pclass" => Binary(0x80, "MyClass") }