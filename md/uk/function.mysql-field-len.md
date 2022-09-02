---
navigation:
  - function.mysql-field-flags.md: « mysqlfieldflags
  - function.mysql-field-name.md: mysqlfieldname »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlfieldlen
---
# mysqlfieldlen

(PHP 4, PHP 5)

mysqlfieldlen — Повертає довжину вказаного поля

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlifetchfielddirect()](mysqli-result.fetch-field-direct.md) length
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) len

### Опис

```methodsynopsis
mysql_field_len(resource $result, int $field_offset): int|false
```

**mysqlfieldlen()** повертає довжину вказаного поля.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.md)

`field_offset`

Числове усунення поля . `field_offset` починається з `0`. Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Довжина зазначеного поля у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlfieldlen()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Не удалось выполнить запрос: ' . mysql_error();
    exit;
}

// Получит длину поля id так, как указано в структуре базы данных
$length = mysql_field_len($result, 0);
echo $length;
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlfieldlen()**

### Дивіться також

-   [mysqlfetchlengths()](function.mysql-fetch-lengths.md) - Повертає довжину кожного поля в результаті
-   [strlen()](function.strlen.md) - Повертає довжину рядка
