---
navigation:
  - function.gmp-sub.md: « gmp\_sub
  - function.gmp-xor.md: gmp\_xor »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_testbit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_testbit

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

gmp\_testbit — Перевірка, чи біт 1

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

Повертає **`true`**, если бит установлен в`num`, иначе\*\*`false`\*\*

### Помилки

Викидається помилка рівня **`E_WARNING`**, якщо `index` менше нуля, і повертається **`false`**

### Приклади

**Пример #1 Пример использования**gmp\_testbit()\*\*\*\*

```php
<?php
$n = gmp_init("1000000");
var_dump(gmp_testbit($n, 1));
gmp_setbit($n, 1);
var_dump(gmp_testbit($n, 1));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [gmp\_setbit()](function.gmp-setbit.md) \- Встановлення біта
-   [gmp\_clrbit()](function.gmp-clrbit.md) \- Скидання біта
