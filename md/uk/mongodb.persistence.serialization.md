Серіалізація у BSON

-   [« Постоянные данные](mongodb.persistence.html)
    
-   [Десериализация из BSON »](mongodb.persistence.deserialization.html)
    
-   [PHP Manual](index.html)
    
-   [Постоянные данные](mongodb.persistence.html)
    
-   Серіалізація у BSON
    

## Серіалізація у BSON

## Масиви

Якщо масив є *упакованим масивом* - тобто порожній масив або якщо ключі починаються з 0 і є послідовними без пробілів: *масив BSON*

Якщо масив не упакований - тобто має асоціативні (рядкові) ключі, ключі не починаються з 0 або за наявності прогалин: *об'єкт BSON*

Документ верхнього рівня (кореневий), *завжди* серіалізується як документ BSON.

## Приклади

Серіалізація як масив BSON:

\=> 0 => 4, 1 => я =>

Серіалізація як документ BSON:

0 => 1, 2 => 8, 3 => 12 => { "0": 1, "2": 8, "3": 12} "foo" => 42 => { "foo" : 42 } 1 => я, 0 => 10 => { "1": я, "0": 10}

Зверніть увагу, що п'ять прикладів є *витримками* з повного документа і подають тільки *одне* значення усередині документа.

## Об'єкти

Якщо об'єкт належить до класу **stdClass**, серіалізуйте, як *документ BSON*

Якщо об'єкт є підтримуваним класом, який реалізує [MongoDB\\BSON\\Type](class.mongodb-bson-type.html)Використовуйте логіку серіалізації BSON для цього конкретного типу. Примірники [MongoDB\\BSON\\Type](class.mongodb-bson-type.html) (виключаючи [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html) можна серіалізувати лише як значення поля документа. Спроба серіалізації такого об'єкта як кореневий документ призведе до викиду [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)

Якщо об'єкт невідомого класу реалізує інтерфейс [MongoDB\\BSON\\Type](class.mongodb-bson-type.html), Видається виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)

Якщо об'єкт відноситься до будь-якого іншого класу, без реалізації будь-якого спеціального інтерфейсу, серіалізуйте, як *документ BSON*. Залишайте тільки *public* властивості та ігноруйте *protected* і *private* властивості.

Якщо об'єкт належить до класу, який реалізує інтерфейс [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html), викличте [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) і використовуйте повернутий масив або **stdClass** для серіалізації як документ BSON або масиву. Тип BSON визначатиметься таким:

1.  Кореневі документи мають бути серіалізовані як документ BSON.
    
2.  [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.html) об'єкти повинні бути серіалізовані як документ BSON.
    
3.  Якщо [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) повертає упакований масив, серіалізуйте його як масив BSON.
    
4.  Якщо [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) повертає невпакований масив або **stdClass**, серіалізуйте як документ BSON.
    
5.  Якщо [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html) не повернув масив або **stdClass**, видасть виняток [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html)
    

Якщо об'єкт належить до класу, який реалізує інтерфейс [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.html) (що має на увазі [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html)), отримайте властивості аналогічно попереднім абзацям, але *також* додайте додаткову властивість pclass як Binary значення з підтипом `0x80` і даними, що містять повне ім'я класу об'єкта, що серіалізується.

Властивість pclass додається в масив або об'єкт, що повертається [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html), що означає, що воно буде перезаписувати будь-який ключ/властивість pclass у значенні, що повертається [MongoDB\\BSON\\Serializable::bsonSerialize()](mongodb-bson-serializable.bsonserialize.html). Якщо ви хочете уникнути такої поведінки та встановити власне значення pclass, ви *не* повинні реалізовувати [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.html) і натомість повинні реалізовувати [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html) безпосередньо.

## Приклади

```php
<?php

class stdClass {
  public $foo = 42;
} // => { "foo" : 42 }

class MyClass {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
} // => { "foo" : 42 }

class AnotherClass1 implements MongoDB\BSON\Serializable {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
  function bsonSerialize(): array {
      return [ 'foo' => $this->foo, 'prot' => $this->prot ];
  }
} // => { "foo" : 42, "prot" : "wine" }

class AnotherClass2 implements MongoDB\BSON\Serializable {
  public $foo = 42;
  function bsonSerialize(): array {
      return $this;
  }
} // => MongoDB\Driver\Exception\UnexpectedValueException("bsonSerialize() did not return an array or stdClass")

class AnotherClass3 implements MongoDB\BSON\Serializable {
  private $elements = [ 'foo', 'bar' ];
  function bsonSerialize(): array {
      return $this->elements;
  }
} // => { "0" : "foo", "1" : "bar" }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass4 implements MongoDB\BSON\Serializable {
    private $elements = [ 0 => 'foo', 2 => 'bar' ];
    function bsonSerialize(): array {
      return $this->elements;
    }
  }
  function bsonSerialize(): array {
      return [ 'things' => $this->things ];
  }
} // => { "things" : { "0" : "foo", "2" : "bar" } }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass5 implements MongoDB\BSON\Serializable {
    private $elements = [ 0 => 'foo', 2 => 'bar' ];
    function bsonSerialize(): array {
      return array_values($this->elements);
    }
  }
  function bsonSerialize(): array {
      return [ 'things' => $this->things ];
  }
} // => { "things" : [ "foo", "bar" ] }

class ContainerClass implements MongoDB\BSON\Serializable {
  public $things = AnotherClass6 implements MongoDB\BSON\Serializable {
    private $elements = [ 'foo', 'bar' ];
    function bsonSerialize(): array {
      return (object) $this->elements;
    }
  }
  function bsonSerialize(): array {
      return [ 'things' => $this->things ];
  }
} // => { "things" : { "0" : "foo", "1" : "bar" } }

class UpperClass implements MongoDB\BSON\Persistable {
  public $foo = 42;
  protected $prot = "wine";
  private $fpr = "cheese";
  function bsonSerialize(): array {
      return [ 'foo' => $this->foo, 'prot' => $this->prot ];
  }
} // => { "foo" : 42, "prot" : "wine", "__pclass" : { "$type" : "80", "$binary" : "VXBwZXJDbGFzcw==" } }
```