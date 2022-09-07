---
navigation:
  - function.gmp-scan1.md: « gmpscan1
  - function.gmp-sign.md: gmpsign »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpsetbit
---
# gmpsetbit

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpsetbit - Встановлення біта

### Опис

```methodsynopsis
gmp_setbit(GMP $num, int $index, bool $value = true): void
```

Встановлює 1 біт з індексом `index` у числі `num`

### Список параметрів

`num`

Значення, що змінюється.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`index`

Індекс встановлюваного біта. Індекс 0 вказує на молодший біт.

`value`

True для установки біта (установки в 1/включено); false для його очищення (установки 0/вимкнено).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)ю

### Приклади

**Приклад #1 Приклад використання **gmpsetbit()** - 0 індекс**

```php
<?php
$a = gmp_init("2"); //
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 0); // 0b10 now becomes 0b11
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

Результат виконання цього прикладу:

```
2 -> 0b10
3 -> 0b11
```

**Приклад #2 Приклад використання **gmpsetbit()** - 1 індекс**

```php
<?php
$a = gmp_init("0xfd");
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 1); // index starts at 0
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

Результат виконання цього прикладу:

```
253 -> 0b11111101
255 -> 0b11111111
```

**Приклад #3 Приклад використання **gmpsetbit()** очищення біта**

```php
<?php
$a = gmp_init("0xff");
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
gmp_setbit($a, 0, false); // clear bit at index 0
echo gmp_strval($a), ' -> 0b', gmp_strval($a, 2), "\n";
?>
```

Результат виконання цього прикладу:

```
255 -> 0b11111111
254 -> 0b11111110
```

### Примітки

> **Зауваження**
> 
> На відміну від більшості GMP функцій, **gmpsetbit()** має викликатися для вже існуючого об'єкта GMP (наприклад, створеного функцією [gmpinit()](function.gmp-init.md)). Число не створюватиметься автоматично.

### Дивіться також

-   [gmpclrbit()](function.gmp-clrbit.md) - Скидання біта
-   [gmptestbit()](function.gmp-testbit.md) - Перевірка, чи встановлений біт в 1
