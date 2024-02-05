---
navigation:
  - function.gmp-divexact.md: « gmp\_divexact
  - function.gmp-fact.md: gmp\_fact »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_export

(PHP 5 >= 5.6.1, PHP 7, PHP 8)

gmp\_export — Експортувати до бінарного рядка

### Опис

```methodsynopsis
gmp_export(GMP|int|string $num, int $word_size = 1, int $flags = GMP_MSW_FIRST | GMP_NATIVE_ENDIAN): string
```

Експортує GMP-число до бінарного рядка

### Список параметрів

`num`

GMP-число для експорту

`word_size`

За замовчуванням дорівнює 1. Кількість байт у кожному блоці бінарних даних. Зазвичай використовується разом із завданням опції.

`flags`

По умолчанию\*\*`GMP_MSW_FIRST`\*\* **`GMP_NATIVE_ENDIAN`**

### Значення, що повертаються

Повертає рядок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не повертає \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Приклад використання** gmp\_export()\*\*\*\*

```php
<?php
$number = gmp_init(16705);
echo gmp_export($number) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
AA
```

### Дивіться також

-   [gmp\_import()](function.gmp-import.md) \- Імпортувати з бінарного рядка
