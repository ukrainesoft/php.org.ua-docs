---
navigation:
  - function.ps-set-text-pos.html: «pssettextpos
  - function.ps-setcolor.html: псsetcolor »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetvalue
---
# псsetvalue

(PECL ps >= 1.1.0)

псsetvalue — Встановлює певні значення

### Опис

```methodsynopsis
ps_set_value(resource $psdoc, string $name, float $value): bool
```

Встановлює декілька значень, що використовуються багатьма функціями. Параметри визначення є значеннями з плаваючою точкою.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`name`

Значення `name` може бути одне з наступного:

textrendering

Спосіб відображення тексту.

textx

Координата X для виведення тексту.

texty

Координата Y для виведення тексту.

wordspacing

Відстань між словами щодо ширини пробілу.

leading

Відстань між рядками у пікселях.

`value`

Значення параметру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псgetvalue()](function.ps-get-value.md) - Отримує певні значення
-   [псsetparameter()](function.ps-set-parameter.md) - Встановлює певні параметри
