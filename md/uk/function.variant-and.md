---
navigation:
  - function.variant-add.md: « variant\_add
  - function.variant-cast.md: variant\_cast »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_and
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_and

(PHP 5, PHP 7, PHP 8)

variant\_and — Побітове І над двома варіантами

### Опис

```methodsynopsis
variant_and(mixed $left, mixed $right): variant
```

Побітове І над двома варіантами. Зверніть увагу, що це звичайна операція І.

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд.

> **Зауваження** :
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за замовчуванням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variant\_add()](function.variant-add.md) у PHP відповідає `VarAdd()`в документации MSDN.

### Значення, що повертаються

**Правила І для варіантів**

| Если `left` равен | и `right` равен | результат будет |
| --- | --- | --- |
| **`true`** | **`true`** | **`true`** |
| **`true`** | **`false`** | **`false`** |
| **`true`** | **`null`** | **`null`** |
| **`false`** | **`true`** | **`false`** |
| **`false`** | **`false`** | **`false`** |
| **`false`** | **`null`** | **`false`** |
| **`null`** | **`true`** | **`null`** |
| **`null`** | **`false`** | **`false`** |
| **`null`** | **`null`** | **`null`** |

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.

### Дивіться також

-   [variant\_or()](function.variant-or.md) \- Побітове АБО над двома варіантами
