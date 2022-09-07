---
navigation:
  - function.ps-setdash.md: «pssetdash
  - function.ps-setfont.md: псsetfont »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetflat
---
# псsetflat

(PECL ps >= 1.1.0)

псsetflat - Встановлює площинність

### Опис

```methodsynopsis
ps_setflat(resource $psdoc, float $value): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`value`

`value` має бути між 0.2 та 1.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
