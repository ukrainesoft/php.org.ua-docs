---
navigation:
  - throwable.tostring.html: '« Throwable::toString'
  - arrayaccess.offsetexists.html: 'ArrayAccess::offsetExists »'
  - index.html: PHP Manual
  - reserved.interfaces.html: Вбудовані інтерфейси та класи
title: Інтерфейс ArrayAccess
---
# Інтерфейс ArrayAccess

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс забезпечує доступ до об'єктів як масивів.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface ArrayAccess {

    /* Методы */
    
   public offsetExists(mixed $offset): bool
public offsetGet(mixed $offset): mixed
public offsetSet(mixed $offset, mixed $value): void
public offsetUnset(mixed $offset): void

   }
```

**Приклад #1 Основи використання**

```php
<?php
class Obj implements ArrayAccess {
    private $container = array();

    public function __construct() {
        $this->container = array(
            "one"   => 1,
            "two"   => 2,
            "three" => 3,
        );
    }

    public function offsetSet($offset, $value) {
        if (is_null($offset)) {
            $this->container[] = $value;
        } else {
            $this->container[$offset] = $value;
        }
    }

    public function offsetExists($offset) {
        return isset($this->container[$offset]);
    }

    public function offsetUnset($offset) {
        unset($this->container[$offset]);
    }

    public function offsetGet($offset) {
        return isset($this->container[$offset]) ? $this->container[$offset] : null;
    }
}

$obj = new Obj;

var_dump(isset($obj["two"]));
var_dump($obj["two"]);
unset($obj["two"]);
var_dump(isset($obj["two"]));
$obj["two"] = "A value";
var_dump($obj["two"]);
$obj[] = 'Append 1';
$obj[] = 'Append 2';
$obj[] = 'Append 3';
print_r($obj);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
int(2)
bool(false)
string(7) "A value"
obj Object
(
    [container:obj:private] => Array
        (
            [one] => 1
            [three] => 3
            [two] => A value
            [0] => Append 1
            [1] => Append 2
            [2] => Append 3
        )

)
```

## Зміст

-   [ArrayAccess::offsetExists](arrayaccess.offsetexists.html) - Визначає, чи існує задане зміщення (ключ)
-   [ArrayAccess::offsetGet](arrayaccess.offsetget.html) — Повертає задане усунення (ключ)
-   [ArrayAccess::offsetSet](arrayaccess.offsetset.html) — Надає значення заданому зміщенню
-   [ArrayAccess::offsetUnset](arrayaccess.offsetunset.html) - Видаляє зміщення
