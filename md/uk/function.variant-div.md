---
navigation:
  - function.variant-date-to-timestamp.html: « variantdateтоtimestamp
  - function.variant-eqv.html: varianteqv »
  - index.md: PHP Manual
  - ref.com.md: Функции COM
title: variantdiv
---
# variantdiv

(PHP 5, PHP 7, PHP 8)

variantdiv — Отримати результат розподілу двох варіантів

### Опис

```methodsynopsis
variant_div(mixed $left, mixed $right): variant
```

ділить `left` на `right` та повертає результат.

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд.

> **Зауваження**
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за умовчанням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variantadd()](function.variant-add.html) у PHP відповідає `VarAdd()` у документації MSDN.

### Значення, що повертаються

**Правила поділу операндів**

| Если | Тогда |
| --- | --- |
| Обидва варіанти - рядки, дати, символи, логічні | Повернеться тип double |
| Один варіант – рядок, а інший – символ | Відбудеться поділ і повернеться тип double |
| Один варіант – число, другий – рядок | Відбудеться поділ і повернеться тип double |
| Обидва варіанти - числа | Відбудеться поділ і повернеться тип double |
| Один з варіантів – NULL | Поверне NULL |
| `right` порожній, а `left` не порожній | Буде викинуто виняток [comexception](class.com-exception.html) з кодом **`DISP_E_DIVBYZERO`** |
| `left` порожній, а `right` не порожній. | Поверне 0 типу double |
| Обидва операнди порожні | Буде викинуто виняток [comexception](class.com-exception.html) з кодом **`DISP_E_OVERFLOW`** |

### Помилки

Викидає виняток [comexception](class.com-exception.html) у разі виникнення помилки.

### Дивіться також

-   [variantidiv()](function.variant-idiv.html) - Перетворення варіантів до цілих з наступним поділом
