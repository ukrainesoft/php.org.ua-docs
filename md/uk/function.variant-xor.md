Виключає АБО над двома варіантами

-   [« variant\_sub](function.variant-sub.html)
    
-   [win32service »](book.win32service.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Виключає АБО над двома варіантами
    

# variantxor

(PHP 5, PHP 7, PHP 8)

variantxor - Виключає АБО над двома варіантами

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

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.html). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variant\_add()](function.variant-add.html) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

**Правила виконання виключає АБО**

| Если `left` | Если `right` | Тогда результат |
|-------------|--------------|-----------------|
| **`true`**  | **`true`**   | **`false`**     |
| **`true`**  | **`false`**  | **`true`**      |
| **`false`** | **`true`**   | **`true`**      |
| **`false`** | **`false`**  | **`false`**     |
| **`null`**  | **`null`**   | **`null`**      |

### Помилки

Викидає виняток [com\_exception](class.com-exception.html) у разі виникнення помилки.

### Дивіться також

-   [variant\_or()](function.variant-or.html) - Побітове АБО над двома варіантами
-   [variant\_and()](function.variant-and.html) - Побітове І над двома варіантами