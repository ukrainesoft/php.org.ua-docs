---
navigation:
  - function.ps-setlinejoin.html: «pssetlinejoin
  - function.ps-setmiterlimit.html: псsetmiterlimit »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetlinewidth
---
# псsetlinewidth

(PECL ps >= 1.1.0)

псsetlinewidth - Встановлює ширину лінії

### Опис

```methodsynopsis
ps_setlinewidth(resource $psdoc, float $width): bool
```

Встановлює ширину лінії для наступних операцій малювання.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`width`

Ширина ліній у точках.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetlinecap()](function.ps-setlinecap.md) - Встановлює зовнішній вигляд закінчення лінії
-   [псsetlinejoin()](function.ps-setlinejoin.md) - Встановлює спосіб з'єднання ліній
-   [псsetmiterlimit()](function.ps-setmiterlimit.md) - Встановлює межу скосу
