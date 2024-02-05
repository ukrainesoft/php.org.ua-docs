---
navigation:
  - function.fdf-get-attachment.md: « fdf\_get\_attachment
  - function.fdf-get-file.md: fdf\_get\_file »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_get\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_get\_encoding

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_get\_encoding — Отримує значення ключа /Encoding

### Опис

```methodsynopsis
fdf_get_encoding(resource $fdf_document): string
```

Получает значение ключа`/Encoding`

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає кодування у вигляді рядка. Повертається порожній рядок, якщо використовується схема за замовчуванням `PDFDocEncoding/Unicode`

### Дивіться також

-   [fdf\_set\_encoding()](function.fdf-set-encoding.md) \- Встановлює кодування символів FDF
