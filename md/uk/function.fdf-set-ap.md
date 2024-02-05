---
navigation:
  - function.fdf-save.md: « fdf\_save
  - function.fdf-set-encoding.md: fdf\_set\_encoding »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_set\_ap
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_set\_ap

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_set\_ap — Встановлює зовнішній вигляд поля

### Опис

```methodsynopsis
fdf_set_ap(    resource $fdf_document,    string $field_name,    int $face,    string $filename,    int $page_number): bool
```

Устанавливает внешний вид поля (т.е. значение ключа`/AP`

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`field_name`

`face`

Допустимі значення: **`FDFNormalAP`** **`FDFRolloverAP`**и**`FDFDownAP`**

`filename`

`page_number`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
