---
navigation:
  - function.odbc-commit.md: « odbc\_commit
  - function.odbc-connection-string-is-quoted.md: odbc\_connection\_string\_is\_quoted »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_connect

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_connect — З'єднує з джерелом даних

### Опис

```methodsynopsis
odbc_connect(    string $dsn,    string $user,    string $password,    int $cursor_option = SQL_CUR_USE_DRIVER): resource|false
```

Ідентифікатор з'єднання, який повертається цією функцією, необхідний для інших ODBC-функцій. Ви можете тримати одночасно відкритими кілька з'єднань.

Деякі ODBC-драйвери, що виконують складні процедури, що зберігаються, можуть обриватися з помилкою типу: "Cannot open a cursor on a stored procedure that has anything other than single select statement in it". Використання SQL\_CUR\_USE\_ODBC допоможе уникнути цієї помилки. Також деякі драйвери не підтримують необов'язковий параметр row\_number в[odbc\_fetch\_row()](function.odbc-fetch-row.md). \_CUR\_USE\_ODBC також може допомогти у цьому випадку.

### Список параметрів

`dsn`

Database Source Name (DSN) для з'єднання. В якості альтернативи можна з'єднуватися і без DSN.

`user`

Ім'я.

`password`

Пароль.

`cursor_option`

Встановлює тип курсора для з'єднання. Зазвичай цей параметр не потрібен, але може бути корисним для обходу проблем із деякими драйверами ODBC.

Наступні константи визначені для курсору:

-   SQL\_CUR\_USE\_IF\_NEEDED
-   SQL\_CUR\_USE\_ODBC
-   SQL\_CUR\_USE\_DRIVER

### Значення, що повертаються

Повертає з'єднання ODBC або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 З'єднання без DSN**

```php
<?php
// Microsoft SQL Server используя SQL Native Client 10.0 ODBC Driver - позволяет соединяться
// с SQL 7, 2000, 2005 и 2008
$connection = odbc_connect("Driver={SQL Server Native Client 10.0};Server=$server;Database=$database;", $user, $password);

// Microsoft Access
$connection = odbc_connect("Driver={Microsoft Access Driver (*.mdb)};Dbq=$mdbFilename", $user, $password);

// Microsoft Excel
$excelFile = realpath('C:/ExcelData.xls');
$excelDir = dirname($excelFile);
$connection = odbc_connect("Driver={Microsoft Excel Driver (*.xls)};DriverId=790;Dbq=$excelFile;DefaultDir=$excelDir" , '', '');
?>
```

### Дивіться також

-   Для постійних з'єднань:[odbc\_pconnect()](function.odbc-pconnect.md) \- Відкриває постійне з'єднання з базою даних
