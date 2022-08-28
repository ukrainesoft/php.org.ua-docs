Визначає, чи існує задане усунення (ключ)

-   [« ArrayAccess](class.arrayaccess.html)
    
-   [ArrayAccess::offsetGet »](arrayaccess.offsetget.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayAccess](class.arrayaccess.html)
    
-   Визначає, чи існує задане усунення (ключ)
    

# ArrayAccess::offsetExists

(PHP 5, PHP 7, PHP 8)

ArrayAccess::offsetExists — Визначає, чи існує зміщення (ключ).

### Опис

```methodsynopsis
public ArrayAccess::offsetExists(mixed $offset): bool
```

Визначає, чи існує дане зміщення (ключ).

Цей метод виконується під час використання [isset()](function.isset.html) або [empty()](function.empty.html) на об'єктах, що реалізують інтерфейс [ArrayAccess](class.arrayaccess.html)

> **Зауваження**
> 
> При використанні функції [empty()](function.empty.html), викликається метод [ArrayAccess::offsetGet()](arrayaccess.offsetget.html) і перевірка на порожнечу відбудеться, тільки якщо метод **ArrayAccess::offsetExists()** поверне **`true`**

### Список параметрів

`offset`

Усунення (ключ) для перевірки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

> **Зауваження**
> 
> Значення, що повертається, буде приведено до логічного типу (bool), якщо значення, що повертається, не є логічним.

### Приклади

**Приклад #1 Приклад використання **ArrayAccess::offsetExists()****

```php
<?php
class obj implements ArrayAccess {
    public function offsetSet($offset, $value): void {
        var_dump(__METHOD__);
    }

    public function offsetExists($var): bool {
        var_dump(__METHOD__);
        if ($var == "foobar") {
            return true;
        }
        return false;
    }

    public function offsetUnset($var): void {
        var_dump(__METHOD__);
    }

    #[ReturnTypeWillChange]
    public function offsetGet($var) {
        var_dump(__METHOD__);
        return "value";
    }
}

$obj = new obj;

echo "Выполняется obj::offsetExists()\n";
var_dump(isset($obj["foobar"]));

echo "\nВыполняется obj::offsetExists() и obj::offsetGet()\n";
var_dump(empty($obj["foobar"]));

echo "\nВыполняется obj::offsetExists(), но *не* obj:offsetGet(), поскольку нечего возвращать\n";
var_dump(empty($obj["foobaz"]));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Выполняется obj::offsetExists()
string(17) "obj::offsetExists"
bool(true)

Выполняется obj::offsetExists() и obj::offsetGet()
string(17) "obj::offsetExists"
string(14) "obj::offsetGet"
bool(false)

Выполняется obj::offsetExists(), но *не* obj:offsetGet(), поскольку нечего возвращать
string(17) "obj::offsetExists"
bool(true)
```