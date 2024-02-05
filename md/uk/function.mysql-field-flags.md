---
navigation:
  - function.mysql-fetch-row.md: « mysql\_fetch\_row
  - function.mysql-field-len.md: mysql\_field\_len »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_field\_flags
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_field\_flags

(PHP 4, PHP 5)

mysql\_field\_flags — Повертає прапори, пов'язані із зазначеним полем результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md) \[flags\]
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) \[flags\]

### Опис

```methodsynopsis
mysql_field_flags(resource $result, int $field_offset): string|false
```

**mysql\_field\_flags()** повертає прапори, пов'язані із зазначеним полем. Кожен прапор повертається як окреме слово, відокремлене від попереднього пропуску. Отримане значення можна розбити на масив, використовуючи функцію [explode()](function.explode.md)

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`field_offset`

Числовое смещение поля`field_offset` починається з . Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок із прапорами, пов'язаними з результатом або \*\*`false`\*\*в случае возникновения ошибки.

Повертаються такі прапори, якщо ваша версія MySQL їх підтримує: `"not_null"` `"primary_key"` `"unique_key"` `"multiple_key"` `"blob"` `"unsigned"` `"zerofill"` `"binary"` `"enum"` `"auto_increment"`и`"timestamp"`

### Приклади

**Пример #1 Пример использования**mysql\_field\_flags()\*\*\*\*

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Ошибка в запросе: ' . mysql_error();
    exit;
}
$flags = mysql_field_flags($result, 0);

echo $flags;
print_r(explode(' ', $flags));
?>
```

Висновок наведеного прикладу буде схожим на:

```
not_null primary_key auto_increment
Array
(
    [0] => not_null
    [1] => primary_key
    [2] => auto_increment
)
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_fieldflags()**

### Дивіться також

-   [mysql\_field\_type()](function.mysql-field-type.md) \- Повертає тип вказаного поля із результату запиту
-   [mysql\_field\_len()](function.mysql-field-len.md) \- Повертає довжину вказаного поля
