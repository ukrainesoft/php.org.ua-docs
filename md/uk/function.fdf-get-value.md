---
navigation:
  - function.fdf-get-status.md: « fdf\_get\_status
  - function.fdf-get-version.md: fdf\_get\_version »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_get\_value
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_get\_value

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_get\_value — Отримує значення поля

### Опис

```methodsynopsis
fdf_get_value(resource $fdf_document, string $fieldname, int $which = -1): mixed
```

Отримує значення запрошеного поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`which`

Елементи поля масиву можна отримати, передавши цей параметр, починаючи з нуля. Для полів без масиву цей параметр буде проігноровано.

### Значення, що повертаються

Повертає значення поля.

### список змін

| Версия | Опис |
| --- | --- |
| 4.3.0 | Додана підтримка масивів та параметра `which` |

### Дивіться також

-   [fdf\_set\_value()](function.fdf-set-value.md) \- Встановлює значення поля
