---
navigation:
  - function.ps-symbol-width.html: «pssymbolwidth
  - function.ps-translate.html: псtranslate »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsymbol
---
# псsymbol

(PECL ps >= 1.2.0)

псsymbol - Виводить гліф

### Опис

```methodsynopsis
ps_symbol(resource $psdoc, int $ord): bool
```

Виводить гліф у позиції `ord` у векторному кодування поточного шрифту. Кодування шрифту можна встановити під час завантаження шрифту за допомогою [псfindfont()](function.ps-findfont.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`ord`

Положення гліфа у векторному шрифт кодування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псsymbolname()](function.ps-symbol-name.md) - Отримує ім'я гліфа
-   [псsymbolwidth()](function.ps-symbol-width.md) - Отримує ширину гліфа
