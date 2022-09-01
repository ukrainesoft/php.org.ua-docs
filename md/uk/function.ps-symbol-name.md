---
navigation:
  - function.ps-stroke.html: «psstroke
  - function.ps-symbol-width.html: псsymbolwidth »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsymbolname
---
# псsymbolname

(PECL ps >= 1.2.0)

псsymbolname — Отримує ім'я гліфа

### Опис

```methodsynopsis
ps_symbol_name(resource $psdoc, int $ord, int $fontid = 0): string
```

Для функції необхідний файл метрик шрифтів Adobe, щоб знати, які гліфи доступні.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`ord`

Параметр `ord` - це позиція гліфа у векторі кодування шрифту.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовуватиметься поточний шрифт.

### Значення, що повертаються

Ім'я гліфа у заданому шрифті.

### Дивіться також

-   [псsymbol()](function.ps-symbol.md) - Виводить гліф
-   [псsymbolwidth()](function.ps-symbol-width.md) - Отримує ширину гліфа
