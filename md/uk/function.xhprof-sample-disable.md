---
navigation:
  - function.xhprof-enable.html: « xhprofenable
  - function.xhprof-sample-enable.html: xhprofsampleenable »
  - index.html: PHP Manual
  - ref.xhprof.html: Функции Xhprof
title: xhprofsampledisable
---
# xhprofsampledisable

(PECL xhprof >= 0.9.0)

xhprofsampledisable — Зупинити профілювання, що семплює, xhprof

### Опис

```methodsynopsis
xhprof_sample_disable(): array
```

Зупинити семплююче профіль xhprof.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив даних, зібраний профайлером.

### Приклади

**Приклад #1 Приклад використання **xhprofsampledisable()****

```php
<?php
xhprof_sample_enable();

for ($i = 0; $i <= 10000; $i++) {
    $a = strlen($i);
    $b = $i * $a;
    $c = rand();
}

$xhprof_data = xhprof_sample_disable();

print_r($xhprof_data);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [1272935300.800000] => main()
    [1272935300.900000] => main()
)
```
