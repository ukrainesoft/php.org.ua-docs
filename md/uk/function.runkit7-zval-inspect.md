---
navigation:
  - function.runkit7-superglobals.md: « runkit7superglobals
  - book.uopz.md: uopz »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7кликавinspect
---
# runkit7кликавinspect

(PECL runkit7> = Unknown)

runkit7кликавinspect — Повертає інформацію про передане значення з типами даних, кількістю посилань і так далі

### Опис

```methodsynopsis
runkit7_zval_inspect(string $value): array
```

### Список параметрів

`value`

Значення, щоб повернути виставу.

### Значення, що повертаються

Масив, що повертається цією функцією, містить такі елементи:

-   `address`
-   `refcount` (Необов'язковий)
-   `is_ref` (Необов'язковий)
-   `type`

### Приклади

**Приклад #1 Приклад використання **runkit7кликавinspect()****

```php
<?php

$var = new DateTime();
var_dump(runkit7_zval_inspect($var));

$var = 1;
var_dump(runkit7_zval_inspect($var));
?>
```

Результат виконання цього прикладу:

```
array(4) {
  ["address"]=>
  string(14) "0x7f45ab21b1e0"
  ["refcount"]=>
  int(2)
  ["is_ref"]=>
  bool(false)
  ["type"]=>
  int(8)
}

array(2) {
  ["address"]=>
  string(14) "0x7f45ab21b1e0"
  ["type"]=>
  int(4)
}
```

### Дивіться також

-   [Пояснення посилань](language.references.md)
-   [» Пояснення посилань (Дерік Ретанс)](http://derickrethans.nl/php_references_article.php)
