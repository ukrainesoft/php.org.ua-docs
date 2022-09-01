---
navigation:
  - function.gmp-sub.html: « gmpsub
  - function.gmp-xor.html: gmpxor »
  - index.html: PHP Manual
  - ref.gmp.html: GMP Функції
title: gmptestbit
---
# gmptestbit

(PHP 5> = 5.3.0, PHP 7, PHP 8)

gmptestbit — Перевірка, чи біт 1

### Опис

```methodsynopsis
gmp_testbit(GMP|int|string $num, int $index): bool
```

Перевіряє, чи встановлено заданий біт 1.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`index`

Перевірений біт

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо біт встановлено в `num`інакше **`false`**

### Помилки

Викидається помилка рівня **`E_WARNING`**, якщо `index` менше нуля, і повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **gmptestbit()****

```php
<?php
$n = gmp_init("1000000");
var_dump(gmp_testbit($n, 1));
gmp_setbit($n, 1);
var_dump(gmp_testbit($n, 1));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [gmpsetbit()](function.gmp-setbit.md) - Встановлення біта
-   [gmpclrbit()](function.gmp-clrbit.md) - Скидання біта
