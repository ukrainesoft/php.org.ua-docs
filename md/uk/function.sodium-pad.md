---
navigation:
  - function.sodium-memzero.md: « sodium\_memzero
  - function.sodium-unpad.md: sodium\_unpad »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_pad
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_pad

(PHP 7 >= 7.2.0, PHP 8)

sodium\_pad — Доповнює рядок відступами

### Опис

```methodsynopsis
sodium_pad(string $string, int $block_size): string
```

Доповнює рядок праворуч до заданої довжини. Безпечна за часом.

### Список параметрів

`string`

Вхідний рядок.

`block_size`

Рядок буде доповнено доти, доки він не стане парною кратною розміру блоку.

### Значення, що повертаються

Доповнений рядок.
