---
navigation:
  - function.variant-or.html: « variantор
  - function.variant-round.html: variantround »
  - index.md: PHP Manual
  - ref.com.md: Функции COM
title: variantpow
---
# variantpow

(PHP 5, PHP 7, PHP 8)

variantpow — Зводить один варіант у ступінь, заданий у другому

### Опис

```methodsynopsis
variant_pow(mixed $left, mixed $right): variant
```

Повертає результат зведення `left` у ступінь `right`

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд (ступінь).

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variantadd()](function.variant-add.md) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

Повертає результат зведення `left` у ступінь `right`

### Помилки

Викидає виняток [comexception](class.com-exception.md) у разі виникнення помилки.

### Дивіться також

-   [pow()](function.pow.md) - Зведення в ступінь
