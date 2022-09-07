---
navigation:
  - function.sodium-increment.md: « sodiumincrement
  - function.sodium-memzero.md: sodiummemzero »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiummemcmp
---
# sodiummemcmp

(PHP 7> = 7.2.0, PHP 8)

sodiummemcmp — Перевірка на рівність за постійну кількість часу

### Опис

```methodsynopsis
sodium_memcmp(string $string1, string $string2): int
```

Порівнює два рядки за постійний час.

Насправді частіше замість цієї функції використовується [hashequals()](function.hash-equals.md)оскільки вона надає ту ж логіку, але повертає логічне значення (bool) замість цілого числа (int). Однак, якщо ви використовуєте значення порівняння, що повертається, в обчисленнях, які чутливі до часу, і турбуєтеся про витікання часу при перетвореннях типу bool-to-int, **sodiummemcmp()** - Ідеальна заміна.

### Список параметрів

`string1`

Рядок для порівняння.

`string2`

Інший рядок для порівняння.

### Значення, що повертаються

Повертає `0`якщо обидва рядки рівні; `-1` в іншому випадку.
