---
navigation:
  - function.gmp-binomial.html: « gmpbinomial
  - function.gmp-cmp.html: gmpcmp »
  - index.html: PHP Manual
  - ref.gmp.html: GMP Функції
title: gmpclrbit
---
# gmpclrbit

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpclrbit - Скидання біта

### Опис

```methodsynopsis
gmp_clrbit(GMP $num, int $index): void
```

Скидає (встановлює 0) біт на позиції `index` аргументу `num`. Індексація починається із 0.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`index`

Індекс біта, що очищається. Індекс 0 вказує на молодший біт.

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.html)ю

### Приклади

**Приклад #1 Приклад використання **gmpclrbit()****

```php
<?php
    $a = gmp_init("0xff");
    gmp_clrbit($a, 0); // индексация с 0, младший значащий бит
    echo gmp_strval($a) . "\n";
    ?>
```

Результат виконання цього прикладу:

```
254
```

### Примітки

> **Зауваження**
> 
> На відміну від більшості GMP функцій, **gmpclrbit()** повинна викликатись для вже існуючого об'єкта GMP (наприклад, створеного за допомогою [gmpinit()](function.gmp-init.html)). Функція не створює їх автоматично.

### Дивіться також

-   [gmpsetbit()](function.gmp-setbit.html) - Встановлення біта
-   [gmptestbit()](function.gmp-testbit.html) - Перевірка, чи встановлений біт в 1
