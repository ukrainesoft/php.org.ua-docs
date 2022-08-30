Повернути цілу частину варіанта

-   [« variantimp](function.variant-imp.html)
    
-   [variantmod »](function.variant-mod.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Повернути цілу частину варіанта
    

# variantint

(PHP 5, PHP 7, PHP 8)

variantint — Повернути цілу частину варіанта

### Опис

```methodsynopsis
variant_int(mixed $value): variant
```

Витягує цілу частину варіанта.

### Список параметрів

`value`

Різновид.

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.html). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variantadd()](function.variant-add.html) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

Якщо `value` від'ємний, то буде повернено перше негативне ціле більше або дорівнює варіанту. У разі позитивного числа буде просто повернена ціла частина `value`

### Помилки

Викидає виняток [comexception](class.com-exception.html) у разі виникнення помилки.

### Дивіться також

-   [variantfix()](function.variant-fix.html) - Повернути цілу частину варіанта
-   [variantround()](function.variant-round.html) - Округлює варіант із заданою точністю
-   [floor()](function.floor.html) - Округлює дріб у менший бік
-   [ceil()](function.ceil.html) - Округлює дріб у велику сторону
-   [round()](function.round.html) - Округлює кількість типу float