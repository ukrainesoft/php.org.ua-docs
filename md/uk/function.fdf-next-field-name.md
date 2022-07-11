- [«fdf_header](function.fdf-header.md)
- [fdf_open_string »](function.fdf-open-string.md)

- [PHP Manual](index.md)
- [FDF](ref.fdf.md)
- Отримує ім'я наступного поля

#fdf_next_field_name

(PHP 4, PHP 5 \< 5.3.0, PECL fdf SVN)

fdf_next_field_name — Отримує ім'я наступного поля

### Опис

**fdf_next_field_name**(resource `$fdf_document`, string `$fieldname` =
?): string

Отримує назву поля після заданого поля. Це ім'я можна використати
декількома функціями.

### Список параметрів

`fdf_document`
Дескриптор документа FDF, що повертається
[fdf_create()](function.fdf-create.md),
[fdf_open()](function.fdf-open.md) або
[fdf_open_string()](function.fdf-open-string.md).

`fieldname`
Ім'я поля FDF у вигляді рядка. Якщо не вказано, використовуватиметься перше
поле.

### Значення, що повертаються

Повертає ім'я поля у вигляді рядка.

### Приклади

**Приклад #1 Виявлення всіх імен полів у FDF**

`<?php$fdf = fdf_open($HTTP_FDF_DATA);for ($field = fdf_next_field_name($fdf);    $field != "";    $field = fdf|$|
";}?> `

### Дивіться також

- [fdf_get_value()](function.fdf-get-value.md) - Отримує значення
поля
