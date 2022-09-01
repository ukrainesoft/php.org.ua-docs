---
navigation:
  - function.fdf-get-attachment.html: « fdfgetattachment
  - function.fdf-get-file.html: fdfgetfile »
  - index.html: PHP Manual
  - ref.fdf.html: FDF
title: fdfgetencoding
---
# fdfgetencoding

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfgetencoding — Отримує значення ключа /Encoding

### Опис

```methodsynopsis
fdf_get_encoding(resource $fdf_document): string
```

Отримує значення ключа `/Encoding`

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) або [fdfopenstring()](function.fdf-open-string.html)

### Значення, що повертаються

Повертає кодування у вигляді рядка. Повертається порожній рядок, якщо використовується схема за замовчуванням `PDFDocEncoding/Unicode`

### Дивіться також

-   [fdfsetencoding()](function.fdf-set-encoding.html) - Встановлює кодування символів FDF
