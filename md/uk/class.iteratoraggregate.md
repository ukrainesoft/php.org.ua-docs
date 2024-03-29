---
navigation:
  - iterator.valid.md: '« Iterator::valid'
  - iteratoraggregate.getiterator.md: 'IteratorAggregate::getIterator »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Інтерфейс IteratorAggregate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс IteratorAggregate

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс створення зовнішнього ітератора.

## Огляд інтерфейсів

```classsynopsis

    
     interface IteratorAggregate

    extends
      Traversable {

    /* Методы */
    
   public getIterator(): Traversable

   }
```

**Приклад #1 Основи використання**

```php
<?php
class myData implements IteratorAggregate {
    public $property1 = "Первое общедоступное свойство";
    public $property2 = "Второе общедоступное свойство";
    public $property3 = "Третье общедоступное свойство";
    public $property4 = "";

    public function __construct() {
        $this->property4 = "последнее свойство";
    }

    public function getIterator(): Traversable {
        return new ArrayIterator($this);
    }
}

$obj = new myData;

foreach($obj as $key => $value) {
    var_dump($key, $value);
    echo "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(9) "property1"
string(56) "Первое общедоступное свойство"

string(9) "property2"
string(56) "Второе общедоступное свойство"

string(9) "property3"
string(56) "Третье общедоступное свойство"

string(9) "property4"
string(35) "последнее свойство"
```

## Зміст

-   [IteratorAggregate::getIterator](iteratoraggregate.getiterator.md)— Отримує зовнішній ітератор
