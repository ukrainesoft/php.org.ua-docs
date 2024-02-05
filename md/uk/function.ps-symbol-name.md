---
navigation:
  - function.ps-stroke.md: « ps\_stroke
  - function.ps-symbol-width.md: ps\_symbol\_width »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_symbol\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_symbol\_name

(PECL ps >= 1.2.0)

ps\_symbol\_name — Отримує ім'я гліфа

### Опис

```methodsynopsis
ps_symbol_name(resource $psdoc, int $ord, int $fontid = 0): string
```

Для функції необхідний файл метрик шрифтів Adobe, щоб знати, які гліфи доступні.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`ord`

Параметр`ord` - це позиція гліфа у векторі кодування шрифту.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовуватиметься поточний шрифт.

### Значення, що повертаються

Ім'я гліфа у заданому шрифті.

### Дивіться також

-   [ps\_symbol()](function.ps-symbol.md) \- Виводить гліф
-   [ps\_symbol\_width()](function.ps-symbol-width.md) \- Отримує ширину гліфа
