---
navigation:
  - function.fdf-get-value.md: « fdf\_get\_value
  - function.fdf-header.md: fdf\_header »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_get\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_get\_version

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_get\_version — Отримує номер версії для FDF API або файлу

### Опис

```methodsynopsis
fdf_get_version(resource $fdf_document = ?): string
```

Якщо параметр не вказано, повертає версію FDF для цього документа або номер версії API набору інструментів.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає версію у вигляді рядка. Для поточного набору інструментів FDF 5.0 номер версії API - `5.0`, а номер версії документа - `1.2` `1.3`или`1.4`

### Дивіться також

-   [fdf\_set\_version()](function.fdf-set-version.md) \- Встановлює номер версії для FDF
