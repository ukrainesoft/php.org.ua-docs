---
navigation:
  - function.variant-eqv.md: « varianteqv
  - function.variant-get-type.md: variantgettype »
  - index.md: PHP Manual
  - ref.com.md: Функции COM
title: variantfix
---
# variantfix

(PHP 5, PHP 7, PHP 8)

variantfix — Повернути цілу частину варіанта

### Опис

```methodsynopsis
variant_fix(mixed $value): variant
```

Повертає цілу частину варіанта.

### Список параметрів

`value`

Різновид.

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variantadd()](function.variant-add.md) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

Якщо `value` від'ємний, то буде повернено перше негативне ціле більше або дорівнює варіанту. У разі позитивного числа буде просто повернена ціла частина `value`

### Помилки

Викидає виняток [comexception](class.com-exception.md) у разі виникнення помилки.

### Примітки

**Увага**

Ви, мабуть, помітили, що опис цієї функції буква в букву збігається з описом функції [variantint()](function.variant-int.md). Так як ця документація заснована на MSDN, то це або так має бути, або в MSDN помилка.

### Дивіться також

-   [variantint()](function.variant-int.md) - Повернути цілу частину варіанта
-   [variantround()](function.variant-round.md) - Округлює варіант із заданою точністю
-   [floor()](function.floor.md) - Округлює дріб у менший бік
-   [ceil()](function.ceil.md) - Округлює дріб у велику сторону
-   [round()](function.round.md) - Округлює кількість типу float
