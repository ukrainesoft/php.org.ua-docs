---
navigation:
  - function.get-mangled-object-vars.md: « get\_mangled\_object\_vars
  - function.get-parent-class.md: get\_parent\_class »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: get\_object\_vars
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_object\_vars

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_object\_vars — Повертає властивості вказаного об'єкта

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

**Приклад #1 Приклад використання** get\_object\_vars()\*\*\*\*

```php
<?php

class foo {
    private $a;
    public $b = 1;
    public $c;
    private $d;
    static $e;

    public function test() {
        var_dump(get_object_vars($this));
    }
}

$test = new foo;
var_dump(get_object_vars($test));

$test->test();

?>
```

Результат виконання наведеного прикладу:

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

> **Зауваження** :
> 
> Неініціалізовані властивості вважаються недоступними і тому не включаються до масиву.

### Дивіться також

-   [get\_class\_methods()](function.get-class-methods.md) \- Повертає масив імен методів класу
-   [get\_class\_vars()](function.get-class-vars.md) \- Повертає оголошені за умовчанням властивості класу
