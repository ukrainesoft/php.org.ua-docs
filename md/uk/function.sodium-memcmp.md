- [« sodium_increment](function.sodium-increment.md)
- [sodium_memzero »](function.sodium-memzero.md)

- [PHP Manual](index.md)
- [Функції Sodium](ref.sodium.md)
- Перевірка на рівність за постійну кількість часу

# sodium_memcmp

(PHP 7 \>= 7.2.0, PHP 8)

sodium_memcmp — Перевірка на рівність за постійну кількість часу

### Опис

**sodium_memcmp**(string `$string1`, string `$string2`): int

Порівнює два рядки за постійний час.

На практиці найчастіше замість цієї функції використовується
[hash_equals()](function.hash-equals.md), оскільки вона надає
ту ж логіку, але повертає логічне значення (bool) замість цілого
числа (int). Однак, якщо ви використовуєте значення порівняння, що повертається
у обчисленнях, які чутливі до часу, і турбуйтеся про
витоків часу при перетвореннях типу bool-to-int,
**sodium_memcmp()** - ідеальна заміна.

### Список параметрів

`string1`
Рядок для порівняння.

`string2`
Інший рядок для порівняння.

### Значення, що повертаються

Повертає `0`, якщо обидва рядки рівні; `-1` інакше.
