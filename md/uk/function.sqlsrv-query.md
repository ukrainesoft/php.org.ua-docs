Готує та виконує запит

-   [« sqlsrvprepare](function.sqlsrv-prepare.html)
    
-   [sqlsrvrollback »](function.sqlsrv-rollback.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SQLSRV](ref.sqlsrv.html)
    
-   Готує та виконує запит
    

# sqlsrvquery

(No version information available, might only be in Git)

sqlsrvquery — Підготовка та виконання запиту

### Опис

```methodsynopsis
sqlsrv_query(    resource $conn,    string $sql,    array $params = ?,    array $options = ?): mixed
```

Підготовляє та виконує запит.

### Список параметрів

`conn`

Ресурс підключення, що повертається [sqlsrvconnect()](function.sqlsrv-connect.html)

`sql`

Рядок, що визначає запит, який потрібно підготувати та виконати.

`params`

Масив, що визначає інформацію про параметри під час виконання параметризованого запиту. Елементи масиву можуть бути будь-якими з наступних:

-   Строкового значення
-   Змінної PHP
-   Масиву з наступною структурою: array($value , $Direction , $phpType , $sqlType

У наступній таблиці описані елементи у структурі масиву вище:

**Структура масиву**

| Элемент               | Описание                                                                                                                                                                         |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| $value                | Рядкове значення, змінна PHP або змінна PHP, передана за посиланням.                                                                                                             |
| $direction (optional) | Одна з наступних констант SQLSRV, що використовуються для вказівки напряму параметра: SQLSRVPARAMIN, SQLSRVPARAMOUT, SQLSRVPARAMINOUT. Значення за промовчанням - SQLSRVPARAMIN. |
| $phpType (optional)   | Константа SQLSRVPHPTYPE, що вказує тип даних PHP значення, що повертається.                                                                                                      |
| $sqlType (optional)   | Константа SQLSRVSQLTYPEвказує тип даних SQL Server вхідного значення.                                                                                                            |

`options`

Масив, що визначає параметри властивостей запиту. Ключі, що підтримуються, описані в наступній таблиці:

**Властивості запиту**

| Ключ                   | Значения                                                                             | Описание                                                                                                                                                                                                                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QueryTimeout           | Позитивне ціле значення.                                                             | Встановлює час очікування в секундах. За замовчуванням драйвер чекатиме на результати нескінченно.                                                                                                                                                                                                         |
| SendStreamParamsAtExec | **`true`** або **`false`** (за замовчуванням **`true`**                              | Налаштовує драйвер для надсилання всіх даних потоку під час виконання (**`true`**) або для надсилання даних потоку частинами (**`false`**). За замовчуванням встановлено значення **`true`**. Для отримання додаткової інформації дивіться [sqlsrvsendstreamdata()](function.sqlsrv-send-stream-data.html) |
| Scrollable             | SQLSRVCURSORFORWARD, SQLSRVCURSORSTATIC, SQLSRVCURSORDYNAMIC, або SQLSRVCURSORKEYSET | Дивіться [» Указание типа курсора и выбор строк](http://msdn.microsoft.com/en-us/library/ee376927.aspx) у документації Microsoft SQLSRV.                                                                                                                                                                   |

### Значення, що повертаються

Повертає ресурс виразу у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvquery()****

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "INSERT INTO Table_1 (id, data) VALUES (?, ?)";
$params = array(1, "some data");

$stmt = sqlsrv_query( $conn, $sql, $params);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}
?>
```

### Примітки

Для операторів, які ви плануєте виконати лише один раз, використовуйте **sqlsrvquery()**. Якщо ви маєте намір повторно виконати вираз з іншими параметрами, використовуйте комбінацію [sqlsrvprepare()](function.sqlsrv-prepare.html) і [sqlsrvexecute()](function.sqlsrv-execute.html)

### Дивіться також

-   [sqlsrvprepare()](function.sqlsrv-prepare.html) - готує запит до виконання
-   [sqlsrvexecute()](function.sqlsrv-execute.html) - Виконує запит підготовлений за допомогою sqlsrvprepare