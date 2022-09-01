---
navigation:
  - function.sqrt.html: « sqrt
  - function.tan.html: tan »
  - index.html: PHP Manual
  - ref.math.html: Математичні функції
title: srand
---
# srand

(PHP 4, PHP 5, PHP 7, PHP 8)

srand - Змінює початкове число генератора псевдовипадкових чисел

### Опис

```methodsynopsis
srand(int $seed = 0, int $mode = MT_RAND_MT19937): void
```

Встановлює початкове число генератора випадкових чисел рівним `seed` або випадковому числу, якщо `seed` дорівнює `0`

> **Зауваження**: Немає необхідності ініціалізувати генератор випадкових чисел функціями **srand()** або [мтsrand()](function.mt-srand.md)оскільки це відбувається автоматично.

> **Зауваження**: Починаючи з PHP 7.1.0, **srand()** стала синонімом функції [мтsrand()](function.mt-srand.md)

### Список параметрів

`seed`

Довільне ціле чисельне (int) початкове значення генератора

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | **srand()** [стала синонимом](migration71.incompatible.html#migration71.incompatible.rand-srand-aliases) функції [мтsrand()](function.mt-srand.md) |

### Приклади

**Приклад #1 Приклад використання **srand()****

```php
<?php
// рандомизировать микросекундами
function make_seed()
{
    list($usec, $sec) = explode(' ', microtime());
    return $sec + $usec * 1000000;
}
srand(make_seed());
$randval = rand();
?>
```

### Дивіться також

-   [rand()](function.rand.md) - Генерує випадкове число
-   [getrandmax()](function.getrandmax.md) - Повертає максимально можливе випадкове число
-   [мтsrand()](function.mt-srand.md) - Проініціалізує генератор випадкових чисел на базі Вихря Мерсенна
