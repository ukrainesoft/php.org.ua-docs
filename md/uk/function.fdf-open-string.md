---
navigation:
  - function.fdf-next-field-name.md: « fdf\_next\_field\_name
  - function.fdf-open.md: fdf\_open »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_open\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_open\_string

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_open\_string — Читає документ FDF з рядка

### Опис

```methodsynopsis
fdf_open_string(string $fdf_data): resource
```

Зчитує дані форми з рядка.

Ви можете використовувати \*\*fdf\_open\_string()\*\*вместе с $HTTP\_FDF\_DATA для обробки введення форми FDF від віддаленого клієнта.

### Список параметрів

`fdf_data`

Дані, повернуті з PDF форми або створені за допомогою [fdf\_create()](function.fdf-create.md) і [fdf\_save\_string()](function.fdf-save-string.md)

### Значення, що повертаються

Повертає дескриптор FDF документа або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Доступ до даних форми**

```php
<?php
$fdf = fdf_open_string($HTTP_FDF_DATA);
/* ... */
fdf_close($fdf);
?>
```

### Дивіться також

-   [fdf\_open()](function.fdf-open.md) \- Відкриває документ FDF
-   [fdf\_close()](function.fdf-close.md) \- Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.md) \- Створює новий документ FDF
-   [fdf\_save\_string()](function.fdf-save-string.md) \- Повертає документ FDF у вигляді рядка
