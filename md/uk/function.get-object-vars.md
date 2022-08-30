Повертає властивості вказаного об'єкту

-   [« getmangledobjectvars](function.get-mangled-object-vars.html)
    
-   [getparentclass »](function.get-parent-class.html)
    
-   [PHP Manual](index.md)
    
-   [Функції роботи з класами та об'єктами](ref.classobj.md)
    
-   Повертає властивості вказаного об'єкту
    

# getobjectvars

(PHP 4, PHP 5, PHP 7, PHP 8)

getobjectvars — Повертає властивості вказаного об'єкта

### Опис

```methodsynopsis
get_object_vars(object $object): array
```

Повертає видимі нестатичні властивості вказаного об'єкта `object` відповідно до області видимості.

### Список параметрів

`object`

Примірник об'єкта

### Значення, що повертаються

Повертає асоціативний масив нестатичних властивостей об'єкту `object`, доступні в даній області видимості.

### Приклади

**Приклад #1 Приклад використання **getobjectvars()****

```php
<?php

class foo {
    private $a;
    public $b = 1;
    public $c;
    private $d;
    static $e;

    public function test() {
        var_dump(get_object_vars($this));
    }
}

$test = new foo;
var_dump(get_object_vars($test));

$test->test();

?>
```

Результат виконання цього прикладу:

```
array(2) {
  ["b"]=>
  int(1)
  ["c"]=>
  NULL
}
array(4) {
  ["a"]=>
  NULL
  ["b"]=>
  int(1)
  ["c"]=>
  NULL
  ["d"]=>
  NULL
}
```

> **Зауваження**
> 
> Неініціалізовані властивості вважаються недоступними і тому не включаються до масиву.

### Дивіться також

-   [getclassmethods()](function.get-class-methods.html) - Повертає масив імен методів класу
-   [getclassvars()](function.get-class-vars.html) - Повертає оголошені за умовчанням властивості класу