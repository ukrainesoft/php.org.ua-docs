---
navigation:
  - function.fdf-save-string.md: « fdf\_save\_string
  - function.fdf-set-ap.md: fdf\_set\_ap »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_save
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_save

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_save — Зберігає документ FDF

### Опис

```methodsynopsis
fdf_save(resource $fdf_document, string $filename = ?): bool
```

Зберігає документ FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

`filename`

Якщо зазначено, FDF буде записаний у цей параметр. В іншому випадку функція запише FDF у вихідний потік PHP за промовчанням.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fdf\_close()](function.fdf-close.md) \- Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.md) \- Створює новий документ FDF
-   [fdf\_save\_string()](function.fdf-save-string.md) \- Повертає документ FDF у вигляді рядка
