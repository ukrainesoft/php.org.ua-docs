---
navigation:
  - function.mysql-field-flags.md: « mysql\_field\_flags
  - function.mysql-field-name.md: mysql\_field\_name »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_field\_len
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_field\_len

(PHP 4, PHP 5)

mysql\_field\_len — Повертає довжину вказаного поля

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_field\_direct()](mysqli-result.fetch-field-direct.md) \[length\]
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.md) \[len\]

### Опис

```methodsynopsis
mysql_field_len(resource $result, int $field_offset): int|false
```

**mysql\_field\_len()** повертає довжину вказаного поля.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`field_offset`

Числовое смещение поля`field_offset` починається з . Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Довжина зазначеного поля у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysql\_field\_len()\*\*\*\*

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Не удалось выполнить запрос: ' . mysql_error();
    exit;
}

// Получит длину поля id так, как указано в структуре базы данных
$length = mysql_field_len($result, 0);
echo $length;
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_fieldlen()**

### Дивіться також

-   [mysql\_fetch\_lengths()](function.mysql-fetch-lengths.md) \- Повертає довжину кожного поля в результаті
-   [strlen()](function.strlen.md) \- Повертає довжину рядка
