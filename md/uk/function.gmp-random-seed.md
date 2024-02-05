---
navigation:
  - function.gmp-random-range.md: « gmp\_random\_range
  - function.gmp-random.md: gmp\_random »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_random\_seed
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_random\_seed

(PHP 7, PHP 8)

gmp\_random\_seed — Встановити початковий стан RNG

### Опис

```methodsynopsis
gmp_random_seed(GMP|int|string $seed): void
```

### Список параметрів

`seed`

Початковий стан для функцій [gmp\_random()](function.gmp-random.md) [gmp\_random\_bits()](function.gmp-random-bits.md) і [gmp\_random\_range()](function.gmp-random-range.md)

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає [ValueError](class.valueerror.md), якщо параметр `seed` вказано некоректно.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Якщо параметр `seed` вказано некоректно, функція **gmp\_random\_seed()** тепер викидає [ValueError](class.valueerror.md); раніше видавалася помилка рівня **`E_WARNING`** і поверталося значення **`false`** |

### Приклади

**Пример #1 Пример использования**gmp\_random\_seed()\*\*\*\*

```php
<?php
// установка начального состояния
gmp_random_seed(100);

var_dump(gmp_strval(gmp_random(1)));

// изменим начальное состояние
gmp_random_seed(gmp_init(-100));

var_dump(gmp_strval(gmp_random_bits(10)));

// зададим некорректное начальное состояние
var_dump(gmp_random_seed('not a number'));
```

Результат виконання наведеного прикладу:

```
string(20) "15370156633245019617"
string(3) "683"

Warning: gmp_random_seed(): Unable to convert variable to GMP - string is not an integer in %s on line %d
bool(false)
```

### Дивіться також

-   [gmp\_init()](function.gmp-init.md) \- Створення GMP числа
-   [gmp\_random()](function.gmp-random.md) \- Випадкове число
-   [gmp\_random\_bits()](function.gmp-random-bits.md) \- Генерує випадкове число
-   [gmp\_random\_range()](function.gmp-random-range.md) \- Отримує рівномірно обране ціле число
