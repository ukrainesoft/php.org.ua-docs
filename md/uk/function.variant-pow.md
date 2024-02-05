---
navigation:
  - function.variant-or.md: « variant\_or
  - function.variant-round.md: variant\_round »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_pow
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_pow

(PHP 5, PHP 7, PHP 8)

variant\_pow — Зводить один варіант у ступінь, заданий у другому

### Опис

```methodsynopsis
variant_pow(mixed $left, mixed $right): variant
```

Возвращает результат возведения`left`в степень`right`

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд (ступінь).

> **Зауваження** :
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за замовчуванням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variant\_add()](function.variant-add.md) у PHP відповідає `VarAdd()`в документации MSDN.

### Значення, що повертаються

Возвращает результат возведения`left`в степень`right`

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.

### Дивіться також

-   [pow()](function.pow.md) \- Зводить у ступінь
