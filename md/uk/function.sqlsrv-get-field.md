Отримує дані поля з поточного вибраного рядка

-   [« sqlsrv\_get\_config](function.sqlsrv-get-config.html)
    
-   [sqlsrv\_has\_rows »](function.sqlsrv-has-rows.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SQLSRV](ref.sqlsrv.html)
    
-   Отримує дані поля з поточного вибраного рядка
    

# sqlsrvgetfield

(No version information available, might only be in Git)

sqlsrvgetfield — Отримує дані поля з поточного вибраного рядка

### Опис

```methodsynopsis
sqlsrv_get_field(resource $stmt, int $fieldIndex, int $getAsType = ?): mixed
```

Отримує дані поля з поточного вибраного рядка. Доступ до полів повинен здійснюватись по порядку. Індекси полів починаються з 0.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrv\_query()](function.sqlsrv-query.html) або [sqlsrv\_execute()](function.sqlsrv-execute.html)

`fieldIndex`

Індекс поля, яке потрібно одержати. Індекси полів починаються з 0. До полів слід звертатися по порядку. тобто. якщо ви звертаєтесь до поля з індексом 1, то індекс поля 0 буде недоступним.

`getAsType`

Тип даних PHP для даних поля, що повертаються. Якщо цей параметр не встановлено, ці поля будуть повернуті як тип даних PHP за промовчанням. Для отримання інформації про типи даних PHP за замовчуванням дивіться [» Типы данных PHP по умолчанию](http://msdn.microsoft.com/en-us/library/cc296193.aspx) у документації Microsoft SQLSRV.

### Значення, що повертаються

У разі успішного виконання повертає дані із вказаного поля. Повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvgetfield()****

У наступному прикладі показано, як отримати рядок за допомогою [sqlsrv\_fetch()](function.sqlsrv-fetch.html) та отримати поля рядки за допомогою **sqlsrvgetfield()**

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Name, Comment
        FROM Table_1
        WHERE ReviewID=1";
$stmt = sqlsrv_query( $conn, $sql);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

// Сделайте первую (и в данном случае единственную) строку набора результатов доступной для чтения.
if( sqlsrv_fetch( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

// Получите поля строки. Индексы полей начинаются с 0 и должны извлекаться по порядку.
// Получение полей строки по имени не поддерживается sqlsrv_get_field.
$name = sqlsrv_get_field( $stmt, 0);
echo "$name: ";

$comment = sqlsrv_get_field( $stmt, 1);
echo $comment;
?>
```

### Дивіться також

-   [sqlsrv\_fetch()](function.sqlsrv-fetch.html) - Робить наступний рядок у наборі результатів доступного для читання
-   [sqlsrv\_fetch\_array()](function.sqlsrv-fetch-array.html) - Повертає рядок як масив
-   [sqlsrv\_fetch\_object()](function.sqlsrv-fetch-object.html) - Отримує наступний рядок даних у наборі результатів як об'єкт