---
navigation:
  - function.fdf-remove-item.md: « fdf\_remove\_item
  - function.fdf-save.md: fdf\_save »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_save\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_save\_string

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_save\_string — Повертає документ FDF у вигляді рядка

### Опис

```methodsynopsis
fdf_save_string(resource $fdf_document): string
```

Повертає документ FDF у вигляді рядка.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md)or[fdf\_open\_string()](function.fdf-open-string.md)

### Значення, що повертаються

Повертає документ у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримання FDF у вигляді рядка**

```php
<?php
$fdf = fdf_create();
fdf_set_value($fdf, "foo", "bar");
$str = fdf_save_string($fdf);
fdf_close($fdf);
echo $str;
?>
```

Результат виконання наведеного прикладу:

```
%FDF-1.2
%âãÏÓ
1 0 obj
<<
/FDF << /Fields 2 0 R >>
>>
endobj
2 0 obj
[
<< /T (foo)/V (bar)>>
]
endobj
trailer
<<
/Root 1 0 R

>>
%%EOF
```

### Дивіться також

-   [fdf\_open\_string()](function.fdf-open-string.md) \- Читає FDF документ з рядка
-   [fdf\_close()](function.fdf-close.md) \- Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.md) \- Створює новий документ FDF
-   [fdf\_save()](function.fdf-save.md) \- Зберігає документ FDF
