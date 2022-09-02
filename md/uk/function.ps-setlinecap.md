---
navigation:
  - function.ps-setgray.md: «pssetgray
  - function.ps-setlinejoin.md: псsetlinejoin »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetlinecap
---
# псsetlinecap

(PECL ps >= 1.1.0)

псsetlinecap - Встановлює зовнішній вигляд закінчення лінії

### Опис

```methodsynopsis
ps_setlinecap(resource $psdoc, int $type): bool
```

Встановлює зовнішній вигляд закінчення лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`type`

Тип закінчення лінії. Можливі значення: `PS_LINECAP_BUTT` `PS_LINECAP_ROUND` або `PS_LINECAP_SQUARED`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetlinejoin()](function.ps-setlinejoin.md) - Встановлює спосіб з'єднання ліній
-   [псsetlinewidth()](function.ps-setlinewidth.md) - Встановлює ширину лінії
-   [псsetmiterlimit()](function.ps-setmiterlimit.md) - Встановлює межу скосу
