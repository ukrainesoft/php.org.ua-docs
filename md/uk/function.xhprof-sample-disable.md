---
navigation:
  - function.xhprof-enable.md: « xhprof\_enable
  - function.xhprof-sample-enable.md: xhprof\_sample\_enable »
  - index.md: PHP Manual
  - ref.xhprof.md: Функції Xhprof
title: xhprof\_sample\_disable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xhprof\_sample\_disable

(PECL xhprof >= 0.9.0)

xhprof\_sample\_disable — Зупинити профілювання, що семплює, xhprof

### Опис

```methodsynopsis
xhprof_sample_disable(): array
```

Зупинити семплюючі профіль xhprof.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив даних, зібраний профайлером.

### Приклади

**Пример #1 Пример использования**xhprof\_sample\_disable()\*\*\*\*

```php
<?php
xhprof_sample_enable();

for ($i = 0; $i <= 10000; $i++) {
    $a = strlen($i);
    $b = $i * $a;
    $c = rand();
}

$xhprof_data = xhprof_sample_disable();

print_r($xhprof_data);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [1272935300.800000] => main()
    [1272935300.900000] => main()
)
```
