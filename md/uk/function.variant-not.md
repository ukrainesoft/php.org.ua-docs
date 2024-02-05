---
navigation:
  - function.variant-neg.md: « variant\_neg
  - function.variant-or.md: variant\_or »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_not
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_not

(PHP 5, PHP 7, PHP 8)

variant\_not - Побитове заперечення над варіантом

### Опис

```methodsynopsis
variant_not(mixed $value): variant
```

Производит побитовое отрицание над`value` і повертає значення, що вийшло.

### Список параметрів

`value`

Варіант.

> **Зауваження** :
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за замовчуванням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variant\_add()](function.variant-add.md) у PHP відповідає `VarAdd()`в документации MSDN.

### Значення, що повертаються

Повертає результат побитового заперечення. Якщо `value`является\*\*`null`\*\*, то результат також буде **`null`**

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.
