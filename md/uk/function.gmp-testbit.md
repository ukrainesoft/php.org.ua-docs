Перевірка, чи встановлений біт в 1

-   [« gmp\_sub](function.gmp-sub.html)
    
-   [gmp\_xor »](function.gmp-xor.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Перевірка, чи встановлений біт в 1
    

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

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`index`

Перевірений біт

### Значення, що повертаються

Повертає **`true`**якщо біт встановлено в `num`інакше **`false`**

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

-   [gmp\_setbit()](function.gmp-setbit.html) - Встановлення біта
-   [gmp\_clrbit()](function.gmp-clrbit.html) - Скидання біта