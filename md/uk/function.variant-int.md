---
navigation:
  - function.variant-imp.md: « variant\_imp
  - function.variant-mod.md: variant\_mod »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_int
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_int

(PHP 5, PHP 7, PHP 8)

variant\_int — Повернути цілу частину варіанта

### Опис

```methodsynopsis
variant_int(mixed $value): variant
```

Витягує цілу частину варіанта.

### Список параметрів

`value`

Варіант.

> **Зауваження** :
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за замовчуванням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variant\_add()](function.variant-add.md) у PHP відповідає `VarAdd()`в документации MSDN.

### Значення, що повертаються

Якщо `value` від'ємний, то буде повернено перше негативне ціле більше або дорівнює варіанту. У разі позитивного числа буде просто повернена ціла частина `value`

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.

### Дивіться також

-   [variant\_fix()](function.variant-fix.md) \- Повернути цілу частину варіанта
-   [variant\_round()](function.variant-round.md) \- Округлює варіант із заданою точністю
-   [floor()](function.floor.md) \- Округлює дробове число у менший бік
-   [ceil()](function.ceil.md) \- Округлює дробове число в більшу сторону
-   [round()](function.round.md) \- Округлює число з плаваючою точкою (float)
