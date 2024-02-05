---
navigation:
  - throwable.tostring.md: '« Throwable::\_\_function toString() { [native code] }'
  - arrayaccess.offsetexists.md: 'ArrayAccess::offsetExists »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Інтерфейс ArrayAccess
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс ArrayAccess

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс дозволяє звертатися до об'єктів як до масивів.

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
class Obj implements ArrayAccess {
    public $container = [
        "one"   => 1,
        "two"   => 2,
        "three" => 3,
    ];

    public function offsetSet($offset, $value): void {
        if (is_null($offset)) {
            $this->container[] = $value;
        } else {
            $this->container[$offset] = $value;
        }
    }

    public function offsetExists($offset): bool {
        return isset($this->container[$offset]);
    }

    public function offsetUnset($offset): void {
        unset($this->container[$offset]);
    }

    public function offsetGet($offset): mixed {
        return isset($this->container[$offset]) ? $this->container[$offset] : null;
    }
}

$obj = new Obj;

var_dump(isset($obj["two"]));
var_dump($obj["two"]);
unset($obj["two"]);
var_dump(isset($obj["two"]));
$obj["two"] = "A value";
var_dump($obj["two"]);
$obj[] = 'Append 1';
$obj[] = 'Append 2';
$obj[] = 'Append 3';
print_r($obj);
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [ArrayAccess::offsetExists](arrayaccess.offsetexists.md) \- Визначає, чи існує задане зміщення (ключ)
-   [ArrayAccess::offsetGet](arrayaccess.offsetget.md)— Повертає задане усунення (ключ)
-   [ArrayAccess::offsetSet](arrayaccess.offsetset.md)— Надає значення заданому зміщенню
-   [ArrayAccess::offsetUnset](arrayaccess.offsetunset.md) \- Видаляє зміщення
