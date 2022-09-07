---
navigation:
  - function.ps-setlinecap.md: «pssetlinecap
  - function.ps-setlinewidth.md: псsetlinewidth »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetlinejoin
---
# псsetlinejoin

(PECL ps >= 1.1.0)

псsetlinejoin - Встановлює спосіб з'єднання ліній

### Опис

```methodsynopsis
ps_setlinejoin(resource $psdoc, int $type): bool
```

Встановлює спосіб з'єднання ліній.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`type`

Спосіб з'єднання ліній. Можливі значення: `PS_LINEJOIN_MITER` `PS_LINEJOIN_ROUND` або `PS_LINEJOIN_BEVEL`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetlinecap()](function.ps-setlinecap.md) - Встановлює зовнішній вигляд закінчення лінії
-   [псsetlinewidth()](function.ps-setlinewidth.md) - Встановлює ширину лінії
-   [псsetmiterlimit()](function.ps-setmiterlimit.md) - Встановлює межу скосу
