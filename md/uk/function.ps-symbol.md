---
navigation:
  - function.ps-symbol-width.md: « ps\_symbol\_width
  - function.ps-translate.md: ps\_translate »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_symbol
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_symbol

(PECL ps >= 1.2.0)

ps\_symbol - Виводить гліф

### Опис

```methodsynopsis
ps_symbol(resource $psdoc, int $ord): bool
```

Виводить гліф у позиції `ord`в векторе кодировки текущего шрифта. Кодировку шрифта можно установить при загрузке шрифта с помощью[ps\_findfont()](function.ps-findfont.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`ord`

Положення гліфа у векторному шрифт кодування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_symbol\_name()](function.ps-symbol-name.md) \- Отримує ім'я гліфа
-   [ps\_symbol\_width()](function.ps-symbol-width.md) \- Отримує ширину гліфа
