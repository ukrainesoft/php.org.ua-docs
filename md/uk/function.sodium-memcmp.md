---
navigation:
  - function.sodium-increment.md: « sodium\_increment
  - function.sodium-memzero.md: sodium\_memzero »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_memcmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_memcmp

(PHP 7 >= 7.2.0, PHP 8)

sodium\_memcmp — Перевірка на рівність за постійну кількість часу

### Опис

```methodsynopsis
sodium_memcmp(string $string1, string $string2): int
```

Порівнює два рядки за постійний час.

Насправді частіше замість цієї функції використовується [hash\_equals()](function.hash-equals.md)оскільки вона надає ту ж логіку, але повертає логічне значення (bool) замість цілого числа (int). Однак, якщо ви використовуєте значення порівняння, що повертається, в обчисленнях, які чутливі до часу, і турбуєтеся про витікання часу при перетвореннях типу bool-to-int, **sodium\_memcmp()** - Ідеальна заміна.

### Список параметрів

`string1`

Рядок для порівняння.

`string2`

Інший рядок для порівняння.

### Значення, що повертаються

Повертає якщо обидва рядки рівні; `-1` в іншому випадку.
