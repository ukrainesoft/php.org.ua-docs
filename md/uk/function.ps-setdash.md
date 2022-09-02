---
navigation:
  - function.ps-setcolor.md: «pssetcolor
  - function.ps-setflat.md: псsetflat »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetdash
---
# псsetdash

(PECL ps >= 1.1.0)

псsetdash - Встановлює зовнішній вигляд пунктирної лінії

### Опис

```methodsynopsis
ps_setdash(resource $psdoc, float $on, float $off): bool
```

Встановлює довжину чорних та білих частин пунктирної лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`on`

Довжина рисочки.

`off`

Довжина проміжку між рисочками.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetpolydash()](function.ps-setpolydash.md) - Встановлює зовнішній вигляд пунктирної лінії
