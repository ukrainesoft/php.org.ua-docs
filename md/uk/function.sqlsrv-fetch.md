---
navigation:
  - function.sqlsrv-fetch-object.md: « sqlsrv\_fetch\_object
  - function.sqlsrv-field-metadata.md: sqlsrv\_field\_metadata »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_fetch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_fetch

(No version information available, might only be in Git)

sqlsrv\_fetch — Робить наступний рядок у наборі результатів, доступних для читання.

### Опис

```methodsynopsis
sqlsrv_fetch(resource $stmt, int $row = ?, int $offset = ?): mixed
```

Делает следующую строку в наборе результатов доступной для чтения. Используйте[sqlsrv\_get\_field()](function.sqlsrv-get-field.md) для читання полів рядка.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrv\_query()](function.sqlsrv-query.md) або [sqlsrv\_execute()](function.sqlsrv-execute.md)

`row`

Рядок, до якого потрібно отримати доступ. Параметр можна використовувати лише в тому випадку, якщо вказаний оператор був підготовлений за допомогою курсору з можливістю прокручування. У цьому випадку параметр може приймати одне з таких значень:

-   SQLSRV\_SCROLL\_NEXT
-   SQLSRV\_SCROLL\_PRIOR
-   SQLSRV\_SCROLL\_FIRST
-   SQLSRV\_SCROLL\_LAST
-   SQLSRV\_SCROLL\_ABSOLUTE
-   SQLSRV\_SCROLL\_RELATIVE

`offset`

Вказує рядок, до якого буде доступ, якщо для параметра рядка встановлено значення \*\*`SQLSRV_SCROLL_ABSOLUTE`**или**`SQLSRV_SCROLL_RELATIVE`\*\*Обратите внимание, что первая строка в наборе результатов имеет индекс 0.

### Значення, що повертаються

Повертає **`true`**, якщо наступний рядок набору результатів було успішно отримано, \*\*`false`**в случае возникновения ошибки и**`null`\*\*якщо у наборі результатів більше немає рядків.

### Приклади

**Пример #1 Пример использования**sqlsrv\_fetch()\*\*\*\*

У наступному прикладі показано, як отримати рядок за допомогою **sqlsrv\_fetch()** та отримати поля рядки за допомогою [sqlsrv\_get\_field()](function.sqlsrv-get-field.md)

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Name, Comment
        FROM Table_1
        WHERE ReviewID=1";
$stmt = sqlsrv_query( $conn, $sql);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

// Сделайте первую (и в данном случае единственную) строку набора результатов доступной для чтения.
if( sqlsrv_fetch( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

// Получите поля строки. Индексы полей начинаются с 0 и должны извлекаться по порядку.
// Получение полей строки по имени не поддерживается sqlsrv_get_field.
$name = sqlsrv_get_field( $stmt, 0);
echo "$name: ";

$comment = sqlsrv_get_field( $stmt, 1);
echo $comment;
?>
```

### Дивіться також

-   [sqlsrv\_get\_field()](function.sqlsrv-get-field.md) \- Отримує дані поля з поточного вибраного рядка
-   [sqlsrv\_fetch\_array()](function.sqlsrv-fetch-array.md) \- Повертає рядок як масив
-   [sqlsrv\_fetch\_object()](function.sqlsrv-fetch-object.md) \- Отримує наступний рядок даних у наборі результатів як об'єкт
