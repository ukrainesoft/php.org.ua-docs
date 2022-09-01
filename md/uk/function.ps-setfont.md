---
navigation:
  - function.ps-setflat.html: «pssetflat
  - function.ps-setgray.html: псsetgray »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: пссетфонт
---
# пссетфонт

(PECL ps >= 1.1.0)

псsetfont — Встановлює шрифт, який буде використовуватись для наступного виводу

### Опис

```methodsynopsis
ps_setfont(resource $psdoc, int $fontid, float $size): bool
```

Встановлює шрифт, який має бути завантажений раніше за допомогою [псfindfont()](function.ps-findfont.md). Виведення тексту без встановлення шрифту призводить до помилки.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`fontid`

Ідентифікатор шрифту, повернутий [псfindfont()](function.ps-findfont.md)

`size`

Розмір шрифту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псfindfont()](function.ps-findfont.md) - Завантажує шрифт
-   [псsettextpos()](function.ps-set-text-pos.md) - Встановлює позицію для виведення тексту на приклад.
