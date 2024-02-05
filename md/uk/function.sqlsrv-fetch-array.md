---
navigation:
  - function.sqlsrv-execute.md: « sqlsrv\_execute
  - function.sqlsrv-fetch-object.md: sqlsrv\_fetch\_object »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_fetch\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_fetch\_array

(No version information available, might only be in Git)

sqlsrv\_fetch\_array — Повертає рядок як масив

### Опис

```methodsynopsis
sqlsrv_fetch_array(    resource $stmt,    int $fetchType = ?,    int $row = ?,    int $offset = ?): array
```

Повертає наступний доступний рядок даних у вигляді асоціативного масиву, числового масиву або того й іншого (за замовчуванням).

### Список параметрів

`stmt`

Ресурс оператора, що повертається sqlsrv\_query або sqlsrv\_prepare.

`fetchType`

Обумовлена ​​константа, що вказує тип масива, що повертається. Можливі значення: **`SQLSRV_FETCH_ASSOC`** **`SQLSRV_FETCH_NUMERIC`**или**`SQLSRV_FETCH_BOTH`**(по умолчанию).

Тип вибірки SQLSRV\_FETCH\_ASSOC не слід використовувати при використанні набору результатів із кількома стовпцями з однаковим ім'ям.

`row`

Задає рядок для доступу в результуючому наборі, в якому використовується курсор, що прокручується. Можливі значення: **`SQLSRV_SCROLL_NEXT`** **`SQLSRV_SCROLL_PRIOR`** **`SQLSRV_SCROLL_FIRST`** **`SQLSRV_SCROLL_LAST`** **`SQLSRV_SCROLL_ABSOLUTE`**и**`SQLSRV_SCROLL_RELATIVE`** (за замовчуванням). Якщо цей параметр вказано, `fetchType` має бути явно визначений.

`offset`

Вказує рядок, до якого буде доступ, якщо для параметра рядка встановлено значення \*\*`SQLSRV_SCROLL_ABSOLUTE`**или**`SQLSRV_SCROLL_RELATIVE`\*\*Обратите внимание, что первая строка в наборе результатов имеет индекс 0.

### Значення, що повертаються

У разі успішного виконання повертає масив, \*\*`null`\*\*якщо в наборі результатів більше немає рядків і \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримання асоціативного масиву.**

```php
<?php
$serverName = "serverName\instanceName";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo );
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT FirstName, LastName FROM SomeTable";
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false) {
    die( print_r( sqlsrv_errors(), true) );
}

while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_ASSOC) ) {
      echo $row['LastName'].", ".$row['FirstName']."<br />";
}

sqlsrv_free_stmt( $stmt);
?>
```

**Приклад #2 Отримання числового масиву.**

```php
<?php
$serverName = "serverName\instanceName";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo );
if( $conn === false ) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT FirstName, LastName FROM SomeTable";
$stmt = sqlsrv_query( $conn, $sql );
if( $stmt === false) {
    die( print_r( sqlsrv_errors(), true) );
}

while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_NUMERIC) ) {
      echo $row[0].", ".$row[1]."<br />";
}

sqlsrv_free_stmt( $stmt);
?>
```

### Примітки

Не вказаний `fetchType` або явне використання константи **`SQLSRV_FETCH_TYPE`** у наведених вище прикладах поверне масив, у якого ключі будуть як асоціативні, і числові.

Якщо більше одного стовпця повертається з тим самим ім'ям, останній стовпець матиме пріоритет. Щоб уникнути конфліктів імен полів, використовуйте псевдоніми.

Якщо стовпець повертається без імені, асоціативний ключ для елемента масиву буде порожнім рядком ("").

### Дивіться також

-   [sqlsrv\_connect()](function.sqlsrv-connect.md) \- Відкриває з'єднання з базою даних Microsoft SQL Server
-   [sqlsrv\_query()](function.sqlsrv-query.md) \- готує та виконує запит
-   [sqlsrv\_errors()](function.sqlsrv-errors.md) \- Повертає інформацію про помилку та попередження останньої виконаної операції SQLSRV
-   [sqlsrv\_fetch()](function.sqlsrv-fetch.md) \- Робить наступний рядок у наборі результатів доступного для читання
