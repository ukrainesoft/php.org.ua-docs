---
navigation:
  - function.unset.md: « unset
  - function.var-export.md: var\_export »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: var\_dump
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# var\_dump

(PHP 4, PHP 5, PHP 7, PHP 8)

var\_dump — Виводить інформацію про змінну

### Опис

```methodsynopsis
var_dump(mixed $value, mixed ...$values): void
```

Функція відображає структуровану інформацію про один або кілька виразів, включаючи їх тип та значення. Масиви та об'єкти аналізуються рекурсивно, значення задаються відступи, щоб показати структуру.

Усі загальнодоступні, закриті та захищені властивості об'єкта будуть повернуті у висновку, крім об'єктів, у яких реалізовано метод [\_\_debugInfo()](language.oop5.magic.md#language.oop5.magic.debuginfo)

**Підказка**

Як і все, що виводить результат у браузер, [функції контролю виведення](book.outcontrol.md) можна викликати, щоб перехопити дані, що виводяться цією функцією, і зберігати їх, наприклад у рядок (string).

### Список параметрів

`value`

Вираз, який треба вивести.

`values`

Наступні вирази висновку.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання функції** var\_dump()\*\*\*\*

```php
<?php

$a = array(1, 2, array("a", "b", "c"));
var_dump($a);
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  array(3) {
    [0]=>
    string(1) "a"
    [1]=>
    string(1) "b"
    [2]=>
    string(1) "c"
  }
}
```

```php
<?php

$b = 3.1;
$c = true;
var_dump($b, $c);

?>
```

Результат виконання наведеного прикладу:

```
float(3.1)
bool(true)
```

### Дивіться також

-   [print\_r()](function.print-r.md) \- Виводить зручну для читання інформацію про змінну
-   [debug\_zval\_dump()](function.debug-zval-dump.md) \- Виводить рядкову виставу внутрішньої структури zval
-   [var\_export()](function.var-export.md) \- Виводить або повертає інтерпретоване рядкове подання змінної
-   [\_\_debugInfo()](language.oop5.magic.md#language.oop5.magic.debuginfo)
