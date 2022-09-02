---
navigation:
  - function.get-class-methods.md: « getclassmethods
  - function.get-class.md: getclass »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: getclassvars
---
# getclassvars

(PHP 4, PHP 5, PHP 7, PHP 8)

getclassvars — Повертає оголошені за умовчанням властивості класу

### Опис

```methodsynopsis
get_class_vars(string $class): array
```

Повертає оголошені за умовчанням властивості зазначеного класу.

### Список параметрів

`class`

Ім'я класу

### Значення, що повертаються

Повертає асоціативний масив оголошених властивостей класу, видимих ​​із поточної області видимості, зі значенням за замовчуванням. Елементи масиву, що виходять, мають форму `varname => value`. У разі виникнення помилки повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **getclassvars()****

```php
<?php

class myclass {

    var $var1; // переменная не имеет начального значения...
    var $var2 = "xyz";
    var $var3 = 100;
    private $var4;

    // конструктор
    function __construct() {
        // изменим значения некоторых свойств
        $this->var1 = "foo";
        $this->var2 = "bar";
        return true;
    }

}

$my_class = new myclass();

$class_vars = get_class_vars(get_class($my_class));

foreach ($class_vars as $name => $value) {
    echo "$name : $value\n";
}

?>
```

Результат виконання цього прикладу:

```
var1 :
var2 : xyz
var3 : 100
```

**Приклад #2 **getclassvars()** та поведінка області видимості**

```php
<?php
function format($array)
{
    return implode('|', array_keys($array)) . "\r\n";
}

class TestCase
{
    public $a    = 1;
    protected $b = 2;
    private $c   = 3;

    public static function expose()
    {
        echo format(get_class_vars(__CLASS__));
    }
}

TestCase::expose();
echo format(get_class_vars('TestCase'));
?>
```

Результат виконання цього прикладу:

```
// 5.0.0
a| * b| TestCase c
a| * b| TestCase c

// 5.0.1 - 5.0.2
a|b|c
a|b|c

// 5.0.3 +
a|b|c
a
```

### Дивіться також

-   [getclassmethods()](function.get-class-methods.md) - Повертає масив імен методів класу
-   [getobjectvars()](function.get-object-vars.md) - Повертає властивості вказаного об'єкту
