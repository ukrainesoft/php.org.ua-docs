---
navigation:
  - function.ps-setmiterlimit.md: «pssetmiterlimit
  - function.ps-setpolydash.md: псsetpolydash »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetoverprintmode
---
# псsetoverprintmode

(PECL ps >= 1.3.0)

псsetoverprintmode — Встановлює режим накладання

### Опис

```methodsynopsis
ps_setoverprintmode(resource $psdoc, int $mode): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`mode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
