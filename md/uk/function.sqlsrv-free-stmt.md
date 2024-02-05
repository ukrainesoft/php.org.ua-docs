---
navigation:
  - function.sqlsrv-field-metadata.md: « sqlsrv\_field\_metadata
  - function.sqlsrv-get-config.md: sqlsrv\_get\_config »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_free\_stmt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_free\_stmt

(No version information available, might only be in Git)

sqlsrv\_free\_stmt — Звільняє всі ресурси для вказаного оператора

### Опис

```methodsynopsis
sqlsrv_free_stmt(resource $stmt): bool
```

Звільняє всі ресурси для вказаного оператора. Оператор не можна використовувати після того, як для нього була викликана функція **sqlsrv\_free\_stmt()**. Якщо **sqlsrv\_free\_stmt()** викликається у операторі, який змінює стан сервера, виконання оператора припиняється і оператор відкочується.

### Список параметрів

`stmt`

Оператор, ресурси якого потрібно звільнити. Зверніть увагу, що **`null`** - Припустиме значення параметра. Це дозволяє викликати функцію у скрипті кілька разів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**sqlsrv\_free\_stmt()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$stmt = sqlsrv_query( $conn, "SELECT * FROM Table_1");
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

/*-------------------------------
     Здесь можно обработать результаты запроса.
-------------------------------*/

/* Освободите ресурсы для оператора */
sqlsrv_free_stmt( $stmt);

?>
```

### Примітки

Основна відмінність між \*\*sqlsrv\_free\_stmt()\*\*и[sqlsrv\_cancel()](function.sqlsrv-cancel.md) полягає в тому, що ресурс оператора, скасований за допомогою [sqlsrv\_cancel()](function.sqlsrv-cancel.md), може бути повторно виконаний, якщо він був створений за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md). Ресурс оператора, скасований за допомогою **sqlsrv\_free\_statement()**, не може бути повторно виконано.

### Дивіться також

-   [sqlsrv\_cancel()](function.sqlsrv-cancel.md) \- скасовує оператор
