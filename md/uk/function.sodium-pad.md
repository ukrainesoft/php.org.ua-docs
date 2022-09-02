---
navigation:
  - function.sodium-memzero.md: « sodiummemzero
  - function.sodium-unpad.md: sodiumunpad »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumpad
---
# sodiumpad

(PHP 7> = 7.2.0, PHP 8)

sodiumpad — Доповнює рядок відступами

### Опис

```methodsynopsis
sodium_pad(string $string, int $block_size): string
```

Доповнює рядок праворуч до заданої довжини. Безпечна за часом.

### Список параметрів

`string`

Вхідний рядок.

`block_size`

Рядок буде доповнено доти, доки вона не стане парною кратною розміру блоку.

### Значення, що повертаються

Доповнений рядок.
