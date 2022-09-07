---
navigation:
  - function.ps-string-geometry.md: «psstringgeometry
  - function.ps-stroke.md: псstroke »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псstringwidth
---
# псstringwidth

(PECL ps >= 1.1.0)

псstringwidth — Отримує ширину рядка

### Опис

```methodsynopsis
ps_stringwidth(    resource $psdoc,    string $text,    int $fontid = 0,    float $size = 0.0): float
```

Обчислює ширину рядка в пунктах, якщо вона виводилася із заданим шрифтом і розміром шрифту. Функції потрібен файл метрик шрифтів Adobe для розрахунку точної ширини. Якщо ввімкнено інтервал між літерами, він також буде врахований.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

`text`

Текст, котрому потрібно розрахувати ширину.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовується поточний шрифт.

`size`

Розмір шрифту. Якщо розмір не вказано, використовується поточний розмір.

### Значення, що повертаються

Ширина рядка у пунктах.

### Дивіться також

-   [псstringgeometry()](function.ps-string-geometry.md) - Отримує геометрію рядка
