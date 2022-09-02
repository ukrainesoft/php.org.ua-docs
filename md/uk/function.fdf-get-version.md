---
navigation:
  - function.fdf-get-value.md: « fdfgetvalue
  - function.fdf-header.md: fdfheader »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdfgetversion
---
# fdfgetversion

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfgetversion — Отримує номер версії для FDF API або файлу

### Опис

```methodsynopsis
fdf_get_version(resource $fdf_document = ?): string
```

Якщо параметр не вказано, повертає версію FDF для цього документа або номер версії API набору інструментів.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.md) [fdfopen()](function.fdf-open.md) або [fdfopenstring()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає версію у вигляді рядка. Для поточного набору інструментів FDF 5.0 номер версії API - `5.0`, а номер версії документа - `1.2` `1.3` або `1.4`

### Дивіться також

-   [fdfsetversion()](function.fdf-set-version.md) - Встановлює номер версії для FDF
