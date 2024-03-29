---
navigation:
  - function.variant-abs.md: « variant\_abs
  - function.variant-and.md: variant\_and »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_add

(PHP 5, PHP 7, PHP 8)

variant\_add — Скласти значення двох варіантів

### Опис

```methodsynopsis
variant_add(mixed $left, mixed $right): variant
```

Складає `left`с`right`, використовуючи такі правила (взято з бібліотеки MSDN), відповідно до Visual Basic:

**Правила складання варіантів**

| Если | То |
| --- | --- |
| Обидва вирази є рядками | Конкатенація |
| Один вираз рядок, а другий - символ | Додавання |
| Один вираз числове, а друге рядкове | Додавання |
| Обидва вирази - числа | Додавання |
| Один із виразів дорівнює NULL | Повернеться NULL |
| Обидва вирази порожні | Повернеться цілий підтип |

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд.

> **Зауваження** :
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за замовчуванням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, **variant\_add()** у PHP відповідає `VarAdd()`в документации MSDN.

### Значення, що повертаються

Повертає результат.

### Помилки

Викидає виняток [com\_exception](class.com-exception.md)в случае возникновения ошибки.

### Дивіться також

-   [variant\_sub()](function.variant-sub.md) \- Віднімає значення правого варіанта з лівого
