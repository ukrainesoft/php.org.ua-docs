---
navigation:
  - function.variant-sub.md: « variant\_sub
  - book.win32service.md: win32service »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_xor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_xor

(PHP 5, PHP 7, PHP 8)

variant\_xor - Виключає АБО над двома варіантами

### Опис

```methodsynopsis
variant_xor(mixed $left, mixed $right): variant
```

Виконання виключає АБО.

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

**Правила виконання виключає АБО**

| Если `left` | Если `right` | Тогда результат |
| --- | --- | --- |
| **`true`** | **`true`** | **`false`** |
| **`true`** | **`false`** | **`true`** |
| **`false`** | **`true`** | **`true`** |
| **`false`** | **`false`** | **`false`** |
| **`null`** | **`null`** | **`null`** |

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.

### Дивіться також

-   [variant\_or()](function.variant-or.md) \- Побітове АБО над двома варіантами
-   [variant\_and()](function.variant-and.md) \- Побітове І над двома варіантами
