---
navigation:
  - ref.ps.md: « Функції PS
  - function.ps-add-launchlink.md: ps\_add\_launchlink »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_add\_bookmark
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_add\_bookmark

(PECL ps >= 1.1.0)

ps\_add\_bookmark — Додає закладку на поточну сторінку

### Опис

```methodsynopsis
ps_add_bookmark(    resource $psdoc,    string $text,    int $parent = 0,    int $open = 0): int
```

Додає закладку до поточної сторінки. Закладки зазвичай видно у програмах перегляду PDF ліворуч від сторінки в ієрархічному дереві. Натискання на закладку відкриває сторінку, на яку вона посилається.

Примітка не відображатиметься під час друку або перегляду документа, але буде показана під час конвертування документа в pdf за допомогою Acrobat Distiller™ або Ghostview.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу, що повертається [ps\_new()](function.ps-new.md), що посилається на postscript-файл.

`text`

Опис закладки.

`parent`

Закладка, створена цією ж функцією, яка буде вказана як батько поточної закладки.

`open`

Якщо `open` не дорівнює нулю, то закладка буде відкриватися при відображенні файлу у програмі перегляду PDF-файлів.

### Значення, що повертаються

Значення, що повертається функцією, є посиланням на закладку. Це посилання використовується у разі побудови ієрархії закладок, якщо потрібно вказати створену закладку як батька. Якщо функція відпрацювала нормально, значення, що повертається, буде більше нуля. Якщо функція завершилася з помилкою, вона поверне нуль.

### Дивіться також

-   [ps\_add\_launchlink()](function.ps-add-launchlink.md) \- Додає посилання, яке запускає файл
-   [ps\_add\_pdflink()](function.ps-add-pdflink.md) \- Додає посилання на сторінку в іншому PDF-документі
-   [ps\_add\_weblink()](function.ps-add-weblink.md) \- Додає посилання на веб-сторінку
