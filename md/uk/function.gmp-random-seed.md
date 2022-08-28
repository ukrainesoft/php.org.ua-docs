Встановити початковий стан RNG

-   [« gmp\_random\_range](function.gmp-random-range.html)
    
-   [gmp\_random »](function.gmp-random.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Встановити початковий стан RNG
    

# gmprandomseed

(PHP 7, PHP 8)

gmprandomseed — Встановити початковий стан RNG

### Опис

```methodsynopsis
gmp_random_seed(GMP|int|string $seed): void
```

### Список параметрів

`seed`

Початковий стан для функцій [gmp\_random()](function.gmp-random.html) [gmp\_random\_bits()](function.gmp-random-bits.html) і [gmp\_random\_range()](function.gmp-random-range.html)

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Виводить **`E_WARNING`** і повертає **`false`**, якщо значення `seed` некоректно.

### Приклади

**Приклад #1 Приклад використання **gmprandomseed()****

```php
<?php
// установка начального состояния
gmp_random_seed(100);

var_dump(gmp_strval(gmp_random(1)));

// изменим начальное состояние
gmp_random_seed(gmp_init(-100));

var_dump(gmp_strval(gmp_random_bits(10)));

// зададим некорректное начальное состояние
var_dump(gmp_random_seed('not a number'));
```

Результат виконання цього прикладу:

```
string(20) "15370156633245019617"
string(3) "683"

Warning: gmp_random_seed(): Unable to convert variable to GMP - string is not an integer in %s on line %d
bool(false)
```

### Дивіться також

-   [gmp\_init()](function.gmp-init.html) - Створення GMP числа
-   [gmp\_random()](function.gmp-random.html) - Випадкове число
-   [gmp\_random\_bits()](function.gmp-random-bits.html) - Випадкове число
-   [gmp\_random\_range()](function.gmp-random-range.html) - Випадкове число