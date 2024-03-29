---
navigation:
  - function.variant-not.md: « variant\_not
  - function.variant-pow.md: variant\_pow »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_or
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_or

(PHP 5, PHP 7, PHP 8)

variant\_or — Побітове АБО над двома варіантами

### Опис

```methodsynopsis
variant_or(mixed $left, mixed $right): variant
```

Побітове АБО над двома варіантами. Зверніть увагу, що функція трохи відрізняється від звичайної операції АБО.

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

**Правила побитового АБО над варіантами**

| Если `left` | Если `right` | Тогда результат |
| --- | --- | --- |
| **`true`** | **`true`** | **`true`** |
| **`true`** | **`false`** | **`true`** |
| **`true`** | **`null`** | **`true`** |
| **`false`** | **`true`** | **`true`** |
| **`false`** | **`false`** | **`false`** |
| **`false`** | **`null`** | **`null`** |
| **`null`** | **`true`** | **`true`** |
| **`null`** | **`false`** | **`null`** |
| **`null`** | **`null`** | **`null`** |

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.

### Дивіться також

-   [variant\_and()](function.variant-and.md) \- Побітове І над двома варіантами
-   [variant\_xor()](function.variant-xor.md) \- що виключає АБО над двома варіантами
