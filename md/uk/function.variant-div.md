---
navigation:
  - function.variant-date-to-timestamp.md: « variant\_date\_to\_timestamp
  - function.variant-eqv.md: variant\_eqv »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_div
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_div

(PHP 5, PHP 7, PHP 8)

variant\_div — Отримати результат розподілу двох варіантів

### Опис

```methodsynopsis
variant_div(mixed $left, mixed $right): variant
```

ділить `left`на`right` та повертає результат.

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

**Правила поділу операндів**

| Если | Тогда |
| --- | --- |
| Обидва варіанти - рядки, дати, символи, логічні | Повернеться тип double |
| Один варіант – рядок, а інший – символ | Відбудеться поділ і повернеться тип double |
| Один варіант – число, другий – рядок | Відбудеться поділ і повернеться тип double |
| Обидва варіанти - числа | Відбудеться поділ і повернеться тип double |
| Один з варіантів – NULL | Поверне NULL |
| `right` порожній, а `left` не порожній | Буде викинуто виняток [com\_exception](class.com-exception.md) з кодом **`DISP_E_DIVBYZERO`** |
| `left` порожній, а `right` не порожній. | Поверне 0 типу double |
| Обидва операнди порожні | Буде викинуто виняток [com\_exception](class.com-exception.md) з кодом **`DISP_E_OVERFLOW`** |

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.

### Дивіться також

-   [variant\_idiv()](function.variant-idiv.md) \- ділить перетворені на цілі числа варіанти
