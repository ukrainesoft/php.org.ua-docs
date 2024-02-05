---
navigation:
  - function.mysql-field-name.md: « mysql\_field\_name
  - function.mysql-field-table.md: mysql\_field\_table »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_field\_seek
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_field\_seek

(PHP 4, PHP 5)

mysql\_field\_seek - Встановлює внутрішній покажчик результату на передане зміщення поля

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_field\_seek()](mysqli-result.field-seek.md)
-   [PDOStatement::fetch()](pdostatement.fetch.md)з використанням параметрів`cursor_orientation`и`offset`

### Опис

```methodsynopsis
mysql_field_seek(resource $result, int $field_offset): bool
```

Переміщує покажчик до поля із зазначеним усуненням. Якщо наступний виклик функції [mysql\_fetch\_field()](function.mysql-fetch-field.md) не містить зміщення, то буде повернено зміщення, що міститься в **mysql\_field\_seek()**

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

`field_offset`

Числовое смещение поля`field_offset` починається з . Якщо `field_offset` не існує, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mysql\_fetch\_field()](function.mysql-fetch-field.md) \- Повертає інформацію про колонку з результату запиту як об'єкта
