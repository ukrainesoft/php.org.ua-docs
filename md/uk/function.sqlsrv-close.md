- [«sqlsrv_client_info](function.sqlsrv-client-info.md)
- [sqlsrv_commit »](function.sqlsrv-commit.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Закриває відкрите з'єднання та звільняє ресурси, пов'язані з
цим з'єднанням

#sqlsrv_close

(No version information available, might only be in Git)

sqlsrv_close — Закриває відкрите з'єднання та звільняє ресурси,
пов'язані з цим з'єднанням

### Опис

**sqlsrv_close**(resource `$conn`): bool

Закриває відкрите з'єднання та звільняє ресурси, пов'язані з цим
з'єднанням.

### Список параметрів

`conn`
З'єднання, яке потрібно закрити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_close()****

` <?php$serverName = "serverName\sqlexpres";$connOptions = array("UID"=>"username", "PWD"=>"password", "Database"=>"dbname");$conn = sqlsrv_connect ( $serverName, $connOptions );if( $conn === false ) {    die( print_r( sqlsrv_errors(), true));}//----------------- --------------------// Виконання операцій з базою даних.//-------------------- -----------------// Закриття з'єднання.sqlsrv_close( $conn );?> `

### Дивіться також

- [sqlsrv_connect()](function.sqlsrv-connect.md) - Відкриває
з'єднання з базою даних Microsoft SQL Server
