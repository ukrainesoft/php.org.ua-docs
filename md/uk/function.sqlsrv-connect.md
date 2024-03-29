---
navigation:
  - function.sqlsrv-configure.md: « sqlsrv\_configure
  - function.sqlsrv-errors.md: sqlsrv\_errors »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_connect

(No version information available, might only be in Git)

sqlsrv\_connect — Відкриває з'єднання з базою даних Microsoft SQL Server

### Опис

```methodsynopsis
sqlsrv_connect(string $serverName, array $connectionInfo = ?): resource
```

Відкриває з'єднання з базою даних Microsoft SQL Server. За промовчанням спроба підключення виконується за допомогою автентифікації Windows. Щоб підключитися з використанням автентифікації SQL Server, увімкніть "UID" і "PWD" в масив параметрів підключення.

### Список параметрів

`serverName`

Ім'я сервера, до якого встановлюється з'єднання. Щоб підключитися до певного екземпляра, після імені сервера вкажіть зворотну косу межу та ім'я екземпляра (наприклад, serverName\\sqlexpress).

`connectionInfo`

Асоціативний масив, який визначає параметри підключення до сервера. Якщо значення для ключів UID і PWD не вказано, буде зроблено спробу підключення за допомогою автентифікації Windows. Повний список підтримуваних ключів дивіться у розділі [» Параметри підключення SQLSRV](http://msdn.microsoft.com/en-us/library/ff628167.aspx)

### Значення, що повертаються

Ресурс підключення. Якщо з'єднання не може бути відкрито, повертається **`false`**

### Приклади

**Приклад #1 Підключення за допомогою автентифікації Windows.**

```php
<?php
$serverName = "serverName\\sqlexpress"; //serverName\instanceName

// Поскольку UID и PWD не указаны в массиве $connectionInfo,
// будет предпринята попытка подключения с использованием проверки подлинности Windows.
$connectionInfo = array( "Database"=>"dbName");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

if( $conn ) {
     echo "Соединение установлено.<br />";
}else{
     echo "Соединение не установлено.<br />";
     die( print_r( sqlsrv_errors(), true));
}
?>
```

**Приклад #2 Підключення за допомогою імені користувача та пароля.**

```php
<?php
$serverName = "serverName\\sqlexpress"; //serverName\instanceName
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

if( $conn ) {
     echo "Соединение установлено.<br />";
}else{
     echo "Соединение не установлено.<br />";
     die( print_r( sqlsrv_errors(), true));
}
?>
```

**Приклад #3 Підключення за допомогою порту.**

```php
<?php
$serverName = "serverName\\sqlexpress, 1542"; //serverName\instanceName, portNumber (по умолчанию 1433)
$connectionInfo = array( "Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

if( $conn ) {
     echo "Соединение установлено.<br />";
}else{
     echo "Соединение не установлено.<br />";
     die( print_r( sqlsrv_errors(), true));
}
?>
```

### Примітки

По умолчанию**sqlsrv\_connect()** використовує пул сполук підвищення продуктивності з'єднання. Щоб вимкнути пул з'єднань (тобто примусово встановлювати нове з'єднання під час кожного виклику), встановіть для параметра "ConnectionPooling" у масиві $connectionOptions значення 0 (або **`false`**). Для отримання додаткової інформації дивіться розділ [» Пул з'єднань SQLSRV](http://msdn.microsoft.com/en-us/library/cc644930.aspx)

Модуль SQLSRV не має спеціальної функції для зміни бази даних після підключення. Цільова база даних вказується в масиві $connectionOptions, що передається в sqlsrv\_connect. Щоб змінити базу даних під час відкритого з'єднання, виконайте наступний запит "USE dbName" (наприклад, sqlsrv\_query($conn, "USE dbName")).

### Дивіться також

-   [sqlsrv\_close()](function.sqlsrv-close.md) \- Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим з'єднанням
-   [sqlsrv\_errors()](function.sqlsrv-errors.md) \- Повертає інформацію про помилку та попередження останньої виконаної операції SQLSRV
-   [sqlsrv\_query()](function.sqlsrv-query.md) \- готує та виконує запит
