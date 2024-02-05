---
navigation:
  - function.variant-cat.md: « variant\_cat
  - function.variant-date-from-timestamp.md: variant\_date\_from\_timestamp »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_cmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_cmp

(PHP 5, PHP 7, PHP 8)

variant\_cmp — Порівняти два варіанти

### Опис

```methodsynopsis
variant_cmp(    mixed $left,    mixed $right,    int $locale_id = LOCALE_SYSTEM_DEFAULT,    int $flags = 0): int
```

Сравнивает`left`с`right`

Функція порівнює лише скалярні величини. Масиви та записи варіантів не порівнює.

### Список параметрів

`left`

Лівий операнд.

`right`

Правий операнд.

`locale_id`

Коректний ідентифікатор локалі, що використовується для порівняння рядків (впливає на сортування рядків).

`flags`

`flags` - побітове АБО наступних значень (або просто одне з них):

**Прапори порівняння варіантів**

| значение | описание |
| --- | --- |
| **`NORM_IGNORECASE`** | Порівнювати реєстронезалежно |
| **`NORM_IGNORENONSPACE`** | Ігнорувати символи, що не займають місця |
| **`NORM_IGNORESYMBOLS`** | Ігнорувати символи |
| **`NORM_IGNOREWIDTH`** | Ігнорувати довжину рядка |
| **`NORM_IGNOREKANATYPE`** | Ігнорувати тип Кану |
| **`NORM_IGNOREKASHIDA`** | Ігнорувати символи Кашиди для Арабської мови |

> **Зауваження** :
> 
> Як і з усіма варіантними арифметичними функціями, параметри цієї функції можуть бути як рідними типами PHP (integer, string, floating point, boolean або **`null`**), і екземплярами класів COM, VARIANT чи DOTNET. Рідні PHP типи будуть перетворені на варіанти (variants) за тими самими правилами, що і в конструкторі класу [variant](class.variant.md). У об'єктів COM і DOTNET буде взято та використано їх значення за замовчуванням як значення варіанта.
> 
> Варіантні арифметичні функції є обертанням навколо однойменних функцій у бібліотеці COM; для більш детальної інформації про ці функції проконсультуйтеся з бібліотекою MSDN. Назви PHP-функцій дещо відрізняються; наприклад, [variant\_add()](function.variant-add.md) у PHP відповідає `VarAdd()`в документации MSDN.

### Значення, що повертаються

Повертає одне з:

**Результати порівняння варіантів**

| значение | описание |
| --- | --- |
| **`VARCMP_LT`** | `left`меньше чем`right` |
| **`VARCMP_EQ`** | `left` ідентичний `right` |
| **`VARCMP_GT`** | `left` більше ніж `right` |
| **`VARCMP_NULL`** | Обидва значення `left`и`right`рівні\*\*`null`\*\* |
