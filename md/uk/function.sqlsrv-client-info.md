- [«sqlsrv_cancel](function.sqlsrv-cancel.md)
- [sqlsrv_close »](function.sqlsrv-close.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Повертає інформацію про клієнта та зазначене підключення

#sqlsrv_client_info

(No version information available, might only be in Git)

sqlsrv_client_info — Повертає інформацію про клієнта та вказане
підключенні

### Опис

**sqlsrv_client_info**(resource `$conn`): array

Повертає інформацію про клієнта та зазначене підключення.

### Список параметрів

`conn`
З'єднання, про яке повертається інформація.

### Значення, що повертаються

Повертає асоціативний масив із ключами, описаними в таблиці нижче. В
в іншому випадку повертає **`false`**.

| Ключ          | Опис                                           |
|---------------|------------------------------------------------|
| DriverDllName | SQLNCLI10.DLL                                  |
| DriverODBCVer | Версія ODBC (xx.yy)                            |
| DriverVer     | Версія SQL Server Native Client DLL (10.5.xxx) |
| ExtensionVer  | Версія php_sqlsrv.dll (2.0.xxx.x)              |

**Масив, що повертається sqlsrv_client_info**

### Приклади

**Приклад #1 Приклад використання **sqlsrv_client_info()****

` <?php$serverName = "serverName\sqlexpress";$connOptions = array("UID"=>"username", "PWD"=>"password");$conn = sqlsrv_connect( $serverName, $connOptions ); ( $conn === false ) {    die( print_r( sqlsrv_errors(), true));}if( $client_info = sqlsrv_client_info( $conn)) {    foreach( $client_info as $key => $value) {        echo $key .": ".$value."<br />"; }} else {    echo "Помилка при отриманні інформації про клієнті.<br />";}?> `

### Дивіться також

- [sqlsrv_server_info()](function.sqlsrv-server-info.md) -
Повертає інформацію про сервер
