---
navigation:
  - function.runkit7-superglobals.md: « runkit7\_superglobals
  - book.uopz.md: uopz »
  - index.md: PHP Manual
  - ref.runkit7.md: Функції runkit7
title: runkit7\_zval\_inspect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# runkit7\_zval\_inspect

(PECL runkit7 >= Unknown)

runkit7\_zval\_inspect — Повертає інформацію про передане значення з типами даних, кількістю посилань і так далі

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

**Пример #1 Пример использования**runkit7\_zval\_inspect()\*\*\*\*

```php
<?php

$var = new DateTime();
var_dump(runkit7_zval_inspect($var));

$var = 1;
var_dump(runkit7_zval_inspect($var));
?>
```

Результат виконання наведеного прикладу:

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
-   [» Пояснення посилань (Дерік Ретанс)](http://derickrethans.nl/php_references_article.php)
