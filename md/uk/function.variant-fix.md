---
navigation:
  - function.variant-eqv.md: « variant\_eqv
  - function.variant-get-type.md: variant\_get\_type »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_fix
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_fix

(PHP 5, PHP 7, PHP 8)

variant\_fix — Повернути цілу частину варіанта

### Опис

```methodsynopsis
variant_fix(mixed $value): variant
```

Повертає цілу частину варіанта.

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

### Примітки

**Увага**

Ви, мабуть, помітили, що опис цієї функції буква в букву збігається з описом функції [variant\_int()](function.variant-int.md). Так як ця документація заснована на MSDN, то це або має бути, або в MSDN помилка.

### Дивіться також

-   [variant\_int()](function.variant-int.md) \- Повернути цілу частину варіанта
-   [variant\_round()](function.variant-round.md) \- Округлює варіант із заданою точністю
-   [floor()](function.floor.md) \- Округлює дробове число у менший бік
-   [ceil()](function.ceil.md) \- Округлює дробове число в більшу сторону
-   [round()](function.round.md) \- Округлює число з плаваючою точкою (float)
