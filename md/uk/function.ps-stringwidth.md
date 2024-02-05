---
navigation:
  - function.ps-string-geometry.md: « ps\_string\_geometry
  - function.ps-stroke.md: ps\_stroke »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_stringwidth
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_stringwidth

(PECL ps >= 1.1.0)

ps\_stringwidth — Отримує ширину рядка

### Опис

```methodsynopsis
ps_stringwidth(    resource $psdoc,    string $text,    int $fontid = 0,    float $size = 0.0): float
```

Обчислює ширину рядка в пунктах, якщо вона виводилася із заданим шрифтом і розміром шрифту. Функції потрібен файл метрик шрифтів Adobe для точної ширини. Якщо ввімкнено інтервал між літерами, він також буде врахований.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`text`

Текст, котрому потрібно розрахувати ширину.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовується поточний шрифт.

`size`

Розмір шрифту. Якщо розмір не вказано, використовується поточний розмір.

### Значення, що повертаються

Ширина рядка у пунктах.

### Дивіться також

-   [ps\_string\_geometry()](function.ps-string-geometry.md) \- Отримує геометрію рядка
