---
navigation:
  - function.ps-set-info.md: «pssetinfo
  - function.ps-set-text-pos.md: псsettextpos »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetparameter
---
# псsetparameter

(PECL ps >= 1.1.0)

псsetparameter — Встановлює певні параметри

### Опис

```methodsynopsis
ps_set_parameter(resource $psdoc, string $name, string $value): bool
```

Встановлює кілька параметрів, які використовують багато функцій. Параметри визначення є строковими значеннями.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`name`

Список можливих імен дивіться [псgetparameter()](function.ps-get-parameter.md)

`value`

Значення параметру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   **псgetparameters()**
-   [псsetvalue()](function.ps-set-value.md) - Встановлює певні значення
