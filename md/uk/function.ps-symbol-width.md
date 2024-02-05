---
navigation:
  - function.ps-symbol-name.md: « ps\_symbol\_name
  - function.ps-symbol.md: ps\_symbol »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_symbol\_width
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_symbol\_width

(PECL ps >= 1.2.0)

ps\_symbol\_width — Отримує ширину гліфа

### Опис

```methodsynopsis
ps_symbol_width(    resource $psdoc,    int $ord,    int $fontid = 0,    float $size = 0.0): float
```

Обчислює ширину гліфа в точках, якщо він був виведений із заданим шрифтом та розміром шрифту. Функції потрібен файл метрик шрифтів Adobe для точної ширини.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`ord`

Положення гліфа у векторному шрифт кодування.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовуватиметься поточний шрифт.

`size`

Розмір шрифту. Якщо розмір не вказано, використовується поточний розмір.

### Значення, що повертаються

Ширина гліфа у точках.

### Дивіться також

-   [ps\_symbol()](function.ps-symbol.md) \- Виводить гліф
-   [ps\_symbol\_name()](function.ps-symbol-name.md) \- Отримує ім'я гліфа
