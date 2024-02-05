---
navigation:
  - mongodb.persistence.md: « Постійні дані
  - mongodb.persistence.deserialization.md: Десеріалізація з BSON »
  - index.md: PHP Manual
  - mongodb.persistence.md: Постійні дані
title: Серіалізація у BSON
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Серіалізація у BSON

## Масиви

Якщо масив є *упакованим масивом* - тобто порожній масив або якщо ключі починаються з 0 і є послідовними без пробілів: *масив BSON*

Якщо масив не упакований - тобто має асоціативні (рядкові) ключі, ключі не починаються з 0 або за наявності прогалин: *об'єкт BSON*

Документ верхнього рівня (кореневий), *завжди*сериализуется, как документ BSON.

## Приклади

Серіалізація як масив BSON:

\[ \] => \[ \]\[ 0 => 4, 1 => 9 \] => \[ \]

Серіалізація як документ BSON:

\[ 0 => 1, 2 => 8, 3 => 12 \] => { "0" : 1, "2" : 8, "3" : 12 } \[ "foo" => 42 \] => { "foo" : 42 } \[ 1 => 9, 0 => 10 \] => { "1" : 9, "0" : 10 }

Зверніть увагу, що п'ять прикладів є *витримками* з повного документа і подають тільки *одне*значение внутри документа.

## . Объекты

Якщо об'єкт належить до класу [stdClass](class.stdclass.md), сериализуйте, как*документ BSON*

Якщо об'єкт є підтримуваним класом, який реалізує [MongoDB\\BSON\\Type](class.mongodb-bson-type.md)Використовуйте логіку серіалізації BSON для цього конкретного типу. Примірники [MongoDB\\BSON\\Type](class.mongodb-bson-type.md) (виключаючи [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.md) можна серіалізувати лише як значення поля документа. Спроба серіалізації такого об'єкта як кореневий документ призведе до викиду [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)

Якщо об'єкт невідомого класу реалізує інтерфейс [MongoDB\\BSON\\Type](class.mongodb-bson-type.md), Видається виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)

Якщо об'єкт відноситься до будь-якого іншого класу, без реалізації будь-якого спеціального інтерфейсу, серіалізуйте, як *документ BSON*Оставляйте только*public* властивості та ігноруйте *protected*и*private*свойства.

Якщо об'єкт належить до класу, який реалізує інтерфейс [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.md), викличте [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md) і використовуйте повернутий масив або [stdClass](class.stdclass.md) для серіалізації як документ BSON або масиву. Тип BSON визначатиметься таким:

1.  Кореневі документи мають бути серіалізовані як документ BSON.
    
2.  [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md)об'єкти повинні бути серіалізовані як документ BSON.
    
3.  Якщо [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md)повертає упакований масив, серіалізуйте його як масив BSON.
    
4.  Якщо [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md)повертає невпакований масив або[stdClass](class.stdclass.md), серіалізуйте як документ BSON.
    
5.  Якщо [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md)не повернув масив або[stdClass](class.stdclass.md), видасть виняток[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)
    

Якщо об'єкт належить до класу, який реалізує інтерфейс [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md) (що має на увазі [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.md)), отримайте властивості аналогічно попереднім абзацям, але *також*добавьте дополнительное свойство\_\_pclass як Binary значення з підтипом `0x80` та даними, що містять повне ім'я класу об'єкта, що серіалізується.

Свойство\_\_pclass додається в масив або об'єкт, що повертається [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md), що означає, що воно буде перезаписувати будь-який ключ/властивість \_\_pclass у значенні, що повертається [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.md). Якщо ви хочете уникнути такої поведінки та встановити власне значення \_\_pclass, ви *не* повинні реалізовувати [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.md) і натомість повинні реалізовувати [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.md)напрямую.

## Приклади

```php
<?php

class stdClass {
  public $foo = 42;
} // => { "foo" : 42 }

class MyClass {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
} // => { "foo" : 42 }

class AnotherClass1 implements MongoDB\BSON\Serializable {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
  function bsonSerialize(): array {
      return [ 'foo' => $this->foo, 'prot' => $this->prot ];
  }
} // => { "foo" : 42, "prot" : "wine" }

class AnotherClass2 implements MongoDB\BSON\Serializable {
  public $foo = 42;
  function bsonSerialize(): array {
      return $this;
  }
} // => MongoDB\Driver\Exception\UnexpectedValueException("bsonSerialize() did not return an array or stdClass")

class AnotherClass3 implements MongoDB\BSON\Serializable {
  private $elements = [ 'foo', 'bar' ];
  function bsonSerialize(): array {
      return $this->elements;
  }
} // => { "0" : "foo", "1" : "bar" }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass4 implements MongoDB\BSON\Serializable {
    private $elements = [ 0 => 'foo', 2 => 'bar' ];
    function bsonSerialize(): array {
      return $this->elements;
    }
  }
  function bsonSerialize(): array {
      return [ 'things' => $this->things ];
  }
} // => { "things" : { "0" : "foo", "2" : "bar" } }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass5 implements MongoDB\BSON\Serializable {
    private $elements = [ 0 => 'foo', 2 => 'bar' ];
    function bsonSerialize(): array {
      return array_values($this->elements);
    }
  }
  function bsonSerialize(): array {
      return [ 'things' => $this->things ];
  }
} // => { "things" : [ "foo", "bar" ] }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass6 implements MongoDB\BSON\Serializable {
    private $elements = [ 'foo', 'bar' ];
    function bsonSerialize(): array {
      return (object) $this->elements;
    }
  }
  function bsonSerialize(): array {
      return [ 'things' => $this->things ];
  }
} // => { "things" : { "0" : "foo", "1" : "bar" } }

class UpperClass implements MongoDB\BSON\Persistable {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
  function bsonSerialize(): array {
      return [ 'foo' => $this->foo, 'prot' => $this->prot ];
  }
} // => { "foo" : 42, "prot" : "wine", "__pclass" : { "$type" : "80", "$binary" : "VXBwZXJDbGFzcw==" } }
```
