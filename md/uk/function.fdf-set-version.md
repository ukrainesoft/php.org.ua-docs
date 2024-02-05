---
navigation:
  - function.fdf-set-value.md: « fdf\_set\_value
  - book.gnupg.md: GnuPG »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_version

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_version — Встановлює номер версії для файлу FDF

### Опис

```methodsynopsis
fdf_set_version(resource $fdf_document, string $version): bool
```

Устанавливает`version`FDF для данного документа.

Деякі функції, які підтримує модуль, доступні лише в нових версіях FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`version`

Номер версії. Для поточного набору інструментів FDF 5.0 це може бути `1.2` `1.3`или`1.4`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fdf\_get\_version()](function.fdf-get-version.md) \- Отримує номер версії для FDF API чи файлу
