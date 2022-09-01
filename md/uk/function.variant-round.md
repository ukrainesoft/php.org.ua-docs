---
navigation:
  - function.variant-pow.html: « variantpow
  - function.variant-set-type.html: variantsettype »
  - index.html: PHP Manual
  - ref.com.html: Функции COM
title: variantround
---
# variantround

(PHP 5, PHP 7, PHP 8)

variantround — Округлює варіант із заданою точністю

### Опис

```methodsynopsis
variant_round(mixed $value, int $decimals): ?variant
```

Повертає значення `value`, заокруглене до `decimals` десяткових знаків.

### Список параметрів

`value`

Різновид.

`decimals`

Точність.

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variantadd()](function.variant-add.md) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

Округлене значення або **`null`** у разі виникнення помилки.

### Дивіться також

-   [round()](function.round.md) - Округлює кількість типу float
