---
navigation:
  - ref.xhprof.md: « Функції Xhprof
  - function.xhprof-enable.md: xhprof\_enable »
  - index.md: PHP Manual
  - ref.xhprof.md: Функції Xhprof
title: xhprof\_disable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xhprof\_disable

(PECL xhprof >= 0.9.0)

xhprof\_disable — Зупиняє профіль xhprof

### Опис

```methodsynopsis
xhprof_disable(): array
```

Зупиняє профіль та повертає зібрані дані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив із результатами профілювання.

### Приклади

**Приклад #1 Приклад використання** xhprof\_disable()\*\*\*\*

```php
<?php
xhprof_enable();

$foo = strlen("foo bar");

$xhprof_data = xhprof_disable();

print_r($xhprof_data);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [main()==>strlen] => Array
        (
            [ct] => 1
            [wt] => 279
        )

    [main()==>xhprof_disable] => Array
        (
            [ct] => 1
            [wt] => 9
        )

    [main()] => Array
        (
            [ct] => 1
            [wt] => 610
        )

)
```
