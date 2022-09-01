---
navigation:
  - function.variant-int.html: « variantint
  - function.variant-mul.html: variantmul »
  - index.html: PHP Manual
  - ref.com.html: Функции COM
title: variantmod
---
# variantmod

(PHP 5, PHP 7, PHP 8)

variantmod - Залишок від поділу двох варіантів

### Опис

```methodsynopsis
variant_mod(mixed $left, mixed $right): variant
```

ділить `left` на `right` та повертає залишок.

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд.

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variantadd()](function.variant-add.md) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

Повертає залишок від поділу.

### Помилки

Викидає виняток [comexception](class.com-exception.md) у разі виникнення помилки.

### Дивіться також

-   [variantdiv()](function.variant-div.md) - Отримати результат розподілу двох варіантів
-   [variantidiv()](function.variant-idiv.md) - Перетворення варіантів до цілих з наступним поділом
