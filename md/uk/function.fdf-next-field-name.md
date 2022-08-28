Отримує ім'я наступного поля

-   [« fdf\_header](function.fdf-header.html)
    
-   [fdf\_open\_string »](function.fdf-open-string.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Отримує ім'я наступного поля
    

# fdfnextfieldname

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfnextfieldname — Отримує ім'я наступного поля

### Опис

```methodsynopsis
fdf_next_field_name(resource $fdf_document, string $fieldname = ?): string
```

Отримує назву поля після заданого поля. Це ім'я можна використовувати кількома функціями.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) або [fdf\_open\_string()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка. Якщо не вказано, використовуватиметься перше поле.

### Значення, що повертаються

Повертає ім'я поля у вигляді рядка.

### Приклади

**Приклад #1 Виявлення всіх імен полів у FDF**

```php
<?php
$fdf = fdf_open($HTTP_FDF_DATA);
for ($field = fdf_next_field_name($fdf);
    $field != "";
    $field = fdf_next_field_name($fdf, $field)) {
    echo "Поле: $field\n";
}
?>
```

### Дивіться також

-   [fdf\_get\_value()](function.fdf-get-value.html) - Отримує значення поля