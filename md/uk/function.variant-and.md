Побітове І над двома варіантами

-   [« variant\_add](function.variant-add.html)
    
-   [variant\_cast »](function.variant-cast.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Побітове І над двома варіантами
    

# variantand

(PHP 5, PHP 7, PHP 8)

variantand — Побітове І над двома варіантами

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

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.html). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variant\_add()](function.variant-add.html) у PHP відповідає `VarAdd()` у документації MSDN.

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

Викидає виняток [com\_exception](class.com-exception.html) у разі виникнення помилки.

### Дивіться також

-   [variant\_or()](function.variant-or.html) - Побітове АБО над двома варіантами