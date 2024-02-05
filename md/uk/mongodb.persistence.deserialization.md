---
navigation:
  - mongodb.persistence.serialization.md: « Серіалізація в BSON
  - mongodb.security.md: Безпека »
  - index.md: PHP Manual
  - mongodb.persistence.md: Постійні дані
title: Десеріалізація з BSON
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Десеріалізація з BSON

**Увага**

Документи BSON технічно можуть містити ключі, що повторюються, оскільки документи зберігаються у вигляді списку пар ключ-значення; однак програмам слід утримуватися від створення документів з дублікатами ключів, оскільки поведінка сервера та драйвера може бути невизначеною. Оскільки об'єкти та масиви PHP не можуть мати ключів, що повторюються, дані також можуть бути втрачені при декодуванні документа BSON з повторюваними ключами.

Устаревший модуль`mongo` десеріалізував як документи, так і масиви BSON як масиви PHP. Хоча з PHP масивами зручно працювати, така поведінка була проблематичною, оскільки різні типи BSON можуть десеріалізуватися до одного і того ж значення PHP (наприклад, `{"0": "foo"}`и`["foo"]`) і неможливо буде вивести оригінальний тип BSON. За промовчанням поточний драйвер вирішує цю проблему, забезпечуючи перетворення масивів та документів BSON на масиви та об'єкти PHP відповідно.

Для складових типів існує три типи даних:

root

відноситься *тільки*к документу верхнего уровня BSON

document

відноситься *тільки* до вбудованих документів BSON

array

відноситься до масивів BSON

Крім трьох групових типів, можна налаштувати певні поля в документі для порівняння з типами даних, вказаними нижче. Як приклад, наступна карта типів дозволяє зіставити кожен вбудований документ у масиві `"addresses"` з класом **Address** *а*каждое поле`"city"` у цих документах із вбудованою адресою з класом **City** :

\[ 'fieldPaths' => \[ 'addresses.$' => 'MyProject\\Address', 'addresses.$.city' => 'MyProject\\City', \],\]

Кожен із цих трьох типів даних, а також зіставлення для конкретних полів можуть бути зіставлені з різними типами PHP. Можливі значення зіставлення:

*не вказано*или NULL (по умолчанию)

-   Масив BSON буде десеріалізовано, як PHP array.
    
-   Документ BSON (кореневий або впроваджений) без якості\_\_pclass[\[1\]](#fnidmongodb.pclass)стає об'єктом PHP[stdClass](class.stdclass.md), причому кожен ключ документа BSON встановлюється як відкрита властивість[stdClass](class.stdclass.md)
    
-   Документ BSON (кореневий або вбудований) з властивістю\_\_pclass[\[1\]](#fnidmongodb.pclass)стає об'єктом PHP імені класу, як це визначено властивістю\_\_pclass.
    
    Якщо цей клас реалізує інтерфейс M[MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md), то властивості документа BSON, включаючи властивість\_\_pclass, відправляються у вигляді асоціативного масиву у функцію[MongoDB\\BSON\\Unserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.md) для ініціалізації властивостей об'єкта
    
    Якщо названий клас не існує або не реалізує інтерфейс[MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md), буде використовуватися[stdClass](class.stdclass.md), і кожен ключ документа BSON (включаючи\_\_pclass) буде встановлено як відкриту властивість[stdClass](class.stdclass.md)
    
    Функціональність\_\_pclass залежить від того, чи є властивістю частиною вилученого документа MongoDB. Якщо ви використовуєте[проекцію](mongodb-driver-query.construct.md#mongodb-driver-query.construct-queryOptions)при запиті документів, потрібно включити поле\_\_pclass у проекцію, щоб ця функція працювала.
    

`"array"`

Перетворює масив BSON або документ BSON на масив PHP. Не буде спеціальної обробки властивості \_\_pclass[\[1\]](#fnidmongodb.pclass), але його можна встановити, як елемент у масиві, що повертається, якщо він був присутній в документі BSON.

`"object"`или`"stdClass"`

Перетворює масив BSON або документ BSON на об'єкт [stdClass](class.stdclass.md). Не буде спеціальної обробки властивості \_\_pclass[\[1\]](#fnidmongodb.pclass), але вона може бути встановлена ​​як відкрита властивість у об'єкті, що повертається, якщо вона була присутня в документі BSON.

`"bson"`

Перетворює BSON масив на [MongoDB\\BSON\\PackedArray](class.mongodb-bson-packedarray.md)и BSON документ в[MongoDB\\BSON\\Document](class.mongodb-bson-document.md), независимо от того, есть ли у BSON документа свойство\_\_pclass[\[1\]](#fnidmongodb.pclass)

> **Зауваження**: Значение`bson` доступне тільки для трьох кореневих типів, але не відображення для конкретних полів.

будь-який інший рядок

Визначає назву класу, який повинен десеріалізувати масив BSON або об'єкт BSON. Для об'єктів BSON, які містять властивості \_\_pclass, цей клас матиме пріоритет.

Якщо названий клас не існує, не є конкретним (тобто абстрактним або інтерфейсом) або не реалізує [MongoDB\\BSON\\Unserializable](class.mongodb-bson-unserializable.md), то видається виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

Якщо об'єкт BSON має властивість \_\_pclass, і цей клас існує та реалізує [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md), він замінить клас, представлений у карті типів.

Свойства документа BSON,*включаючи*свойство\_\_pclass, якщо воно існує, буде відправлено у вигляді асоціативного масиву в функцію [MongoDB\\BSON\\Unserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.md) для ініціалізації властивостей об'єкта

## TypeMaps

TypeMaps можно установить с помощью метода[MongoDB\\Driver\\Cursor::setTypeMap()](mongodb-driver-cursor.settypemap.md) для об'єкту [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.md)или аргумента`$typeMap`в[MongoDB\\BSON\\toPHP()](function.mongodb.bson-tophp.md) [MongoDB\\BSON\\Document::toPHP()](mongodb-bson-document.tophp.md) і [MongoDB\\BSON\\PackedArray::toPHP()](mongodb-bson-packedarray.tophp.md). Кожен із трьох класів (*root* *document*, и*array*) може бути заданий індивідуально, на додаток до типів полів.

Якщо значення на карті дорівнює NULL, це означає те саме, що і значення *за замовчуванням* для цього елемента.

## Приклади

У цих прикладах використовуються такі класи:

MyClass

Котрий *не* реалізує інтерфейс

YourClass

який реалізує [MongoDB\\BSON\\Unserializable](class.mongodb-bson-unserializable.md)

OurClass

який реалізує [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md)

TheirClass

який розширює OurClass

Метод[MongoDB\\BSON\\Unserializable::bsonUnserialize()](mongodb-bson-unserializable.bsonunserialize.md) класу YourClass, OurClass, OurClass виконує ітерацію за масивом та встановлює властивості без змін. Він *також*устанавливает для свойства`$unserialized`значение\*\*`true`\*\* :

```php
<?php

function bsonUnserialize( array $map )
{
    foreach ( $map as $k => $value )
    {
        $this->$k = $value;
    }
    $this->unserialized = true;
}
```

\*typemap:\[\](все значения по умолчанию)\*/ { "foo": "yes", "bar" : false } -> stdClass { $foo => 'yes', $bar => false }

{ "foo": "no", "array" : \[ \] } -> stdClass { $foo => 'no', $array => \[ \]

{ "foo": "no", "obj" : { "embedded" : 3.14 } } -> stdClass { $foo => 'no', $obj => stdClass { $embedded => 3.14 } }

{ "foo": "yes", "\_\_pclass": "MyClass" } -> stdClass { $foo => 'yes', $\_\_pclass => 'MyClass' }

{ "foo": "yes", "\_\_pclass": { "$type" : "80", "$binary" : "MyClass" } } -> stdClass { $foo => 'yes', $\_\_pclass => Binary(0x80, 'MyClass') }

{ "foo": "yes", "\_\_pclass": { "$type" : "80", "$binary" : "YourClass") } -> stdClass { $foo => 'yes', $\_\_pclass => Binary(0x80, 'YourClass') }

{ "foo": "yes", "\_\_pclass": { "$type" : "80", "$binary" : "OurClass") } -> OurClass { $foo => 'yes', $\_\_pclass => Binary(0x80, 'OurClass'), $unserialized => true }

{ "foo": "yes", "\_\_pclass": { "$type" : "44", "$binary" : "YourClass") } -> stdClass { $foo => 'yes', $\_\_pclass => Binary(0x44, 'YourClass') }

\*typemap:\[ "root" => "MissingClass" \] \*/ { "foo": "yes" } -> MongoDB\\Driver\\Exception\\InvalidArgumentException("MissingClass does not exist")

\*typemap:\[ "root" => "MyClass" \] \*/ { "foo": "yes", "\_\_pclass" : { "$type": "80", "$binary": "MyClass" } } -> MongoDB\\Driver\\Exception\\InvalidArgumentException("MyClass does not implement Unserializable interface")

\*typemap:\[ "root" => "MongoDB\\BSON\\Unserializable" \] \*/ { "foo": "yes" } -> MongoDB\\Driver\\Exception\\InvalidArgumentException("Unserializable is not a concrete class")

\*typemap:\[ "root" => "YourClass" \] \*/ { "foo": "yes", "\_\_pclass" : { "$type": "80", "$binary": "MongoDB\\BSON\\Unserializable" } } -> YourClass { $foo => "yes", $\_\_pclass => Binary(0x80, "MongoDB\\BSON\\Unserializable"), $unserialized => true }

\*typemap:\[ "root" => "YourClass" \] \*/ { "foo": "yes", "\_\_pclass" : { "$type": "80", "$binary": "MyClass" } } -> YourClass { $foo => "yes", $\_\_pclass => Binary(0x80, "MyClass"), $unserialized => true }

\*typemap:\[ "root" => "YourClass" \] \*/ { "foo": "yes", "\_\_pclass" : { "$type": "80", "$binary": "OurClass" } } -> OurClass { $foo => "yes", $\_\_pclass => Binary(0x80, "OurClass"), $unserialized => true }

\*typemap:\[ "root" => "YourClass" \] \*/ { "foo": "yes", "\_\_pclass" : { "$type": "80", "$binary": "TheirClass" } } -> TheirClass { $foo => "yes", $\_\_pclass => Binary(0x80, "TheirClass"), $unserialized => true }

\*typemap:\[ "root" => "OurClass" \] \*/ { foo: "yes", "\_\_pclass" : { "$type": "80", "$binary": "TheirClass" } } -> TheirClass { $foo => "yes", $\_\_pclass => Binary(0x80, "TheirClass"), $unserialized => true }

\*typemap:\[ 'root' => 'YourClass' \] \*/ { foo: "yes", "\_\_pclass" : { "$type": "80", "$binary": "YourClass" } } -> YourClass { $foo => 'yes', $\_\_pclass => Binary(0x80, 'YourClass'), $unserialized => true }

\*typemap:\[ 'root' => 'array', 'document' => 'array' \] \*/ { "foo": "yes", "bar" : false } -> \[ "foo" => "yes", "bar" => false \]

{ "foo": "no", "array" : \[ \] } -> \[ "foo" => "no", "array" => \[ \] \]

{ "foo": "no", "obj" : { "embedded" : 3.14 } } -> \[ "foo" => "no", "obj" => \[ "embedded => 3.14 \] \]

{ "foo": "yes", "\_\_pclass": "MyClass" } -> \[ "foo" => "yes", "\_\_pclass" => "MyClass" \]

{ "foo": "yes", "\_\_pclass" : { "$type": "80", "$binary": "MyClass" } } -> \[ "foo" => "yes", "\_\_pclass" => Binary(0x80, "MyClass") \]

{ "foo": "yes", "\_\_pclass" : { "$type": "80", "$binary": "OurClass" } } -> \[ "foo" => "yes", "\_\_pclass" => Binary(0x80, "OurClass") \]

\*typemap:\[ 'root' => 'object', 'document' => 'object' \] \*/ { "foo": "yes", "\_\_pclass": { "$type": "80", "$binary": "MyClass" } } -> stdClass { $foo => "yes", "\_\_pclass" => Binary(0x80, "MyClass") }
