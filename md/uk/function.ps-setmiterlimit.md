---
navigation:
  - function.ps-setlinewidth.md: «pssetlinewidth
  - function.ps-setoverprintmode.md: псsetoverprintmode »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsetmiterlimit
---
# псsetmiterlimit

(PECL ps >= 1.1.0)

псsetmiterlimit - Встановлює межу скосу

### Опис

```methodsynopsis
ps_setmiterlimit(resource $psdoc, float $value): bool
```

Якщо дві лінії з'єднуються під невеликим кутом, а для з'єднання ліній встановлено значення `PS_LINEJOIN_MITER`, То результуючий виступ буде дуже довгим. Межа скосу - це максимальне співвідношення довжини скосу (довжини виступу) та ширини лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

`value`

Максимальне співвідношення між довжиною скосу та шириною лінії. Великі значення (> 10) призведуть до дуже довгих виступів, якщо дві лінії перетинаються під невеликим кутом. Залишіть значення за промовчанням, якщо ви не впевнені, що робите.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsetlinecap()](function.ps-setlinecap.md) - Встановлює зовнішній вигляд закінчення лінії
-   [псsetlinejoin()](function.ps-setlinejoin.md) - Встановлює спосіб з'єднання ліній
-   [псsetlinewidth()](function.ps-setlinewidth.md) - Встановлює ширину лінії
