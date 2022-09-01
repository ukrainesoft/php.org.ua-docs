---
navigation:
  - function.variant-cast.html: « variantcast
  - function.variant-cmp.html: variantcmp »
  - index.md: PHP Manual
  - ref.com.md: Функции COM
title: variantcat
---
# variantcat

(PHP 5, PHP 7, PHP 8)

variantcat - Об'єднання (конкатенація) значень двох варіантів

### Опис

```methodsynopsis
variant_cat(mixed $left, mixed $right): variant
```

Об'єднує `left` з `right` та повертає результат.

Функція еквівалентна виконанню `$left` `.` `$right`

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд.

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variantadd()](function.variant-add.html) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

Повертає результат об'єднання.

### Помилки

Викидає виняток [comexception](class.com-exception.html) у разі виникнення помилки.

### Дивіться також

-   [Рядкові оператори](language.operators.string.md) - конкатенація рядків
