---
navigation:
  - function.ps-add-locallink.html: «psaddlocallink
  - function.ps-add-pdflink.html: псaddpdflink »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псaddnote
---
# псaddnote

(PECL ps >= 1.1.0)

псaddnote — Додає нотатку до поточної сторінки

### Опис

```methodsynopsis
ps_add_note(    resource $psdoc,    float $llx,    float $lly,    float $urx,    float $ury,    string $contents,    string $title,    string $icon,    int $open): bool
```

Додає примітку до певного місця на сторінці. Примітки нагадують маленькі прямокутні аркуші з текстом, які можна розмістити в будь-якому місці сторінки. Вони показані у згорнутому чи розгорнутому вигляді. У згорнутому вигляді зазначений значок використовується як заповнювач.

Примітка не відображатиметься під час друку або перегляду документа, але буде показана під час конвертування документа в pdf за допомогою Acrobat Distiller™ або Ghostview.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

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

Значок відображається, якщо нотатка складена. Може бути: `comment` `insert` `note` `paragraph` `newparagraph` `key` або `help`

`open`

Якщо `open` не дорівнює нулю, нотатка буде відображатися розгорнутою після відкриття документа за допомогою програми перегляду PDF.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псaddpdflink()](function.ps-add-pdflink.html) - Додає посилання на сторінку в іншому PDF-документі
-   [псaddlaunchlink()](function.ps-add-launchlink.html) - Додає посилання, яке запускає файл
-   [псaddlocallink()](function.ps-add-locallink.html) - Додає посилання на сторінку того самого документа
-   [псaddweblink()](function.ps-add-weblink.html) - Додає посилання на веб-сторінку
