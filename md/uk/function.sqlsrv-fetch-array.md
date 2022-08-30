Повертає рядок як масив

-   [« sqlsrvexecute](function.sqlsrv-execute.html)
    
-   [sqlsrvfetchobject »](function.sqlsrv-fetch-object.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SQLSRV](ref.sqlsrv.md)
    
-   Повертає рядок як масив
    

# sqlsrvfetcharray

(No version information available, might only be in Git)

sqlsrvfetcharray — Повертає рядок як масив

### Опис

```methodsynopsis
sqlsrv_fetch_array(    resource $stmt,    int $fetchType = ?,    int $row = ?,    int $offset = ?): array
```

Повертає наступний доступний рядок даних у вигляді асоціативного масиву, числового масиву або й того й іншого (за умовчанням).

### Список параметрів

`stmt`

Ресурс оператора, що повертається sqlsrvquery або sqlsrvprepare.

`fetchType`

Обумовлена ​​константа, що вказує тип масива, що повертається. Можливі значення: **`SQLSRV_FETCH_ASSOC`** **`SQLSRV_FETCH_NUMERIC`** або **`SQLSRV_FETCH_BOTH`** (за замовчуванням).

Тип вибірки SQLSRVFETCHASSOC не слід використовувати при використанні набору результатів із кількома стовпцями з однаковим ім'ям.

`row`

Задає рядок для доступу в результуючому наборі, в якому використовується курсор, що прокручується. Можливі значення: **`SQLSRV_SCROLL_NEXT`** **`SQLSRV_SCROLL_PRIOR`** **`SQLSRV_SCROLL_FIRST`** **`SQLSRV_SCROLL_LAST`** **`SQLSRV_SCROLL_ABSOLUTE`** і **`SQLSRV_SCROLL_RELATIVE`** (за замовчуванням). Якщо цей параметр вказано, `fetchType` має бути явно визначений.

`offset`

Вказує рядок, до якого буде доступ, якщо для параметра рядка встановлено значення **`SQLSRV_SCROLL_ABSOLUTE`** або **`SQLSRV_SCROLL_RELATIVE`**. Зауважте, що перший рядок у наборі результатів має індекс 0.

### Значення, що повертаються

У разі успішного виконання повертає масив, \*\*`null`\*\*якщо в наборі результатів більше немає рядків і **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримання асоціативного масиву.**

```php
<?php
$serverName = "serverName\instanceName";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo );
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT FirstName, LastName FROM SomeTable";
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false) {
    die( print_r( sqlsrv_errors(), true) );
}

while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_ASSOC) ) {
      echo $row['LastName'].", ".$row['FirstName']."<br />";
}

sqlsrv_free_stmt( $stmt);
?>
```

**Приклад #2 Отримання числового масиву.**

```php
<?php
$serverName = "serverName\instanceName";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo );
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT FirstName, LastName FROM SomeTable";
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false) {
    die( print_r( sqlsrv_errors(), true) );
}

while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_NUMERIC) ) {
      echo $row[0].", ".$row[1]."<br />";
}

sqlsrv_free_stmt( $stmt);
?>
```

### Примітки

Не вказаний `fetchType` або явне використання константи **`SQLSRV_FETCH_TYPE`** у наведених вище прикладах поверне масив, у якого ключі будуть як асоціативні, і числові.

Якщо більше одного стовпця повертається з тим самим ім'ям, останній стовпець матиме пріоритет. Щоб уникнути конфліктів імен полів, використовуйте псевдоніми.

Якщо стовпець повертається без імені, асоціативний ключ для елемента масиву буде порожнім рядком ("").

### Дивіться також

-   [sqlsrvconnect()](function.sqlsrv-connect.html) - Відкриває з'єднання з базою даних Microsoft SQL Server
-   [sqlsrvquery()](function.sqlsrv-query.html) - готує та виконує запит
-   [sqlsrverrors()](function.sqlsrv-errors.html) - Повертає інформацію про помилку та попередження останньої виконаної операції SQLSRV
-   [sqlsrvfetch()](function.sqlsrv-fetch.html) - Робить наступний рядок у наборі результатів доступного для читання