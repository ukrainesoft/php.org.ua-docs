---
navigation:
  - function.fdf-header.md: « fdf\_header
  - function.fdf-open-string.md: fdf\_open\_string »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_next\_field\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_next\_field\_name

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_next\_field\_name — Отримує ім'я наступного поля

### Опис

```methodsynopsis
fdf_next_field_name(resource $fdf_document, string $fieldname = ?): string
```

Отримує назву поля після заданого поля. Це ім'я можна використовувати кількома функціями.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.md) [fdf\_open()](function.fdf-open.md) або [fdf\_open\_string()](function.fdf-open-string.md)

`fieldname`

Ім'я поля FDF у вигляді рядка. Якщо не вказано, використовуватиметься перше поле.

### Значення, що повертаються

Повертає ім'я поля у вигляді рядка.

### Приклади

**Приклад #1 Виявлення всіх імен полів у FDF**

```php
<?php
$fdf = fdf_open($HTTP_FDF_DATA);
for ($field = fdf_next_field_name($fdf);
    $field != "";
    $field = fdf_next_field_name($fdf, $field)) {
    echo "Поле: $field\n";
}
?>
```

### Дивіться також

-   [fdf\_get\_value()](function.fdf-get-value.md) \- Отримує значення поля
