---
navigation:
  - function.gmp-hamdist.md: « gmp\_hamdist
  - function.gmp-init.md: gmp\_init »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_import
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_import

(PHP 5 >= 5.6.1, PHP 7, PHP 8)

gmp\_import — Імпортувати з бінарного рядка

### Опис

```methodsynopsis
gmp_import(string $data, int $word_size = 1, int $flags = GMP_MSW_FIRST | GMP_NATIVE_ENDIAN): GMP
```

Імпортує GMP-число з бінарного рядка

### Список параметрів

`data`

Бінарний рядок для імпорту

`word_size`

За замовчуванням дорівнює 1. Кількість байт у кожному блоці бінарних даних. Зазвичай використовується разом із завданням опції.

`flags`

По умолчанию\*\*`GMP_MSW_FIRST`\*\* **`GMP_NATIVE_ENDIAN`**

### Значення, що повертаються

Повертає GMP-число.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не повертає \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Приклад використання** gmp\_import()\*\*\*\*

```php
<?php
$number = gmp_import("\0");
echo gmp_strval($number) . "\n";

$number = gmp_import("\0\1\2");
echo gmp_strval($number) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
0
258
```

### Дивіться також

-   [gmp\_export()](function.gmp-export.md) \- Експортувати до бінарного рядка
