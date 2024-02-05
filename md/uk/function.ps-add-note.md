---
navigation:
  - function.ps-add-locallink.md: « ps\_add\_locallink
  - function.ps-add-pdflink.md: ps\_add\_pdflink »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_add\_note
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_add\_note

(PECL ps >= 1.1.0)

ps\_add\_note — Додає нотатку до поточної сторінки

### Опис

```methodsynopsis
ps_add_note(    resource $psdoc,    float $llx,    float $lly,    float $urx,    float $ury,    string $contents,    string $title,    string $icon,    int $open): bool
```

Додає примітку до певного місця на сторінці. Примітки схожі на маленькі прямокутні аркуші з текстом, які можна розмістити у будь-якому місці сторінки. Вони показані у згорнутому чи розгорнутому вигляді. У згорнутому вигляді зазначений значок використовується як заповнювач.

Примітка не відображатиметься під час друку або перегляду документа, але буде показана під час конвертування документа в pdf за допомогою Acrobat Distiller™ або Ghostview.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`llx`

Координата X лівого нижнього кута.

`lly`

Координата Y лівого нижнього кута.

`urx`

Координата X правого верхнього кута.

`ury`

Координата Y правого верхнього кута.

`contents`

Примітка тексту.

`title`

Назва примітки, що відображається у заголовку примітки.

`icon`

Значок відображається, якщо нотатка складена. Може бути: `comment` `insert` `note` `paragraph` `newparagraph` `key`или`help`

`open`

Якщо `open` не дорівнює нулю, нотатка буде відображатися розгорнутою після відкриття документа за допомогою програми перегляду PDF.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_add\_pdflink()](function.ps-add-pdflink.md) \- Додає посилання на сторінку в іншому PDF-документі
-   [ps\_add\_launchlink()](function.ps-add-launchlink.md) \- Додає посилання, яке запускає файл
-   [ps\_add\_locallink()](function.ps-add-locallink.md) \- Додає посилання на сторінку того самого документа
-   [ps\_add\_weblink()](function.ps-add-weblink.md) \- Додає посилання на веб-сторінку
