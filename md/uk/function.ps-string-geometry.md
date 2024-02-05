---
navigation:
  - function.ps-show.md: « ps\_show
  - function.ps-stringwidth.md: ps\_stringwidth »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_string\_geometry
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_string\_geometry

(PECL ps >= 1.2.0)

ps\_string\_geometry — Отримує геометрію рядка

### Опис

```methodsynopsis
ps_string_geometry(    resource $psdoc,    string $text,    int $fontid = 0,    float $size = 0.0): array
```

Функция похожа на[ps\_stringwidth()](function.ps-stringwidth.md), але повертає масив розмірів, що містить ширину, верхню та нижню межу тексту.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`text`

Текст, для якого має бути розрахована геометрія.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовується поточний шрифт.

`size`

Розмір шрифту. Якщо розмір не вказано, використовується поточний розмір.

### Значення, що повертаються

Масив розмірів рядка. Елемент "width" містить ширину рядка, що повертається функцією [ps\_stringwidth()](function.ps-stringwidth.md). . Елемент "descender" містить максимальну нижню межу, а "ascender" - максимальну верхню межу елемента рядка.

### Дивіться також

-   [ps\_continue\_text()](function.ps-continue-text.md) \- Продовжує текст у наступному рядку
-   [ps\_stringwidth()](function.ps-stringwidth.md) \- Отримує ширину рядка
