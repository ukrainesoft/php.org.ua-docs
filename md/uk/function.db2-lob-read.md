---
navigation:
  - function.db2-last-insert-id.html: « db2lastinsertід
  - function.db2-next-result.html: db2nextresult »
  - index.html: PHP Manual
  - ref.ibm-db2.html: Функції IBM DB2
title: db2лобread
---
# db2лобread

(PECL ibmdb2> = 1.6.0)

db2лобread — Отримує певний користувачем розмір LOB-файлів під час кожного виклику

### Опис

```methodsynopsis
db2_lob_read(resource $stmt, int $colnum, int $length): string
```

Використовуйте **db2лобread()** для ітерації за вказаним стовпцем набору результатів та отримання заданого користувачем розміру LOB-даних.

### Список параметрів

`stmt`

Допустимий ресурс `stmt`містить LOB-дані.

`colnum`

Допустимий номер стовпця у наборі результатів ресурсу `stmt`

`length`

Розмір LOB-даних, що витягуються з ресурсу `stmt`

### Значення, що повертаються

Повертає кількість даних, вказаних користувачем. Повертає \*\*`false`\*\*якщо дані не можуть бути отримані.

### Приклади

**Приклад #1 Ітерації з різних типів даних**

```php
<?php

/* Параметры подключения к базе данных */
$db = 'SAMPLE';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Получение ресурса подключения */
$conn = db2_connect($db,$username,$password);

if ($conn) {
    $drop = 'DROP TABLE clob_stream';
    $result = @db2_exec( $conn, $drop );

    $create = 'CREATE TABLE clob_stream (id INTEGER, my_clob CLOB)';
    $result = db2_exec( $conn, $create );

    $variable = "";
    $stmt = db2_prepare($conn, "INSERT INTO clob_stream (id,my_clob) VALUES (1, ?)");
    $variable = "THIS IS A CLOB TEST. THIS IS A CLOB TEST.";
    db2_bind_param($stmt, 1, "variable", DB2_PARAM_IN);
    db2_execute($stmt);

    $sql = "SELECT id,my_clob FROM clob_stream";
    $result = db2_prepare($conn, $sql);
    db2_execute($result);
    db2_fetch_row($result);
    $i = 0;
    /* Чтение LOB-данных */
    while ($data = db2_lob_read($result, 2, 6)) {
        echo "Loop $i: $data\n";
        $i = $i + 1;
    }

    $drop = 'DROP TABLE blob_stream';
    $result = @db2_exec( $conn, $drop );

    $create = 'CREATE TABLE blob_stream (id INTEGER, my_blob CLOB)';
    $result = db2_exec( $conn, $create );

    $variable = "";
    $stmt = db2_prepare($conn, "INSERT INTO blob_stream (id,my_blob) VALUES (1, ?)");
    $variable = "THIS IS A BLOB TEST. THIS IS A BLOB TEST.";
    db2_bind_param($stmt, 1, "variable", DB2_PARAM_IN);
    db2_execute($stmt);

    $sql = "SELECT id,my_blob FROM blob_stream";
    $result = db2_prepare($conn, $sql);
    db2_execute($result);
    db2_fetch_row($result);
    $i = 0;
    /* Чтенеи LOB-данных */
    while ($data = db2_lob_read($result, 2, 6)) {
        echo "Loop $i: $data\n";
        $i = $i + 1;
    }
} else {
    echo 'Нет соединения: ' . db2_conn_errormsg();
}

?>
```

Результат виконання цього прикладу:

```
Loop 0: THIS I
Loop 1: S A CL
Loop 2: OB TES
Loop 3: T. THI
Loop 4: S IS A
Loop 5:  CLOB
Loop 6: TEST.
Loop 0: THIS I
Loop 1: S A BL
Loop 2: OB TES
Loop 3: T. THI
Loop 4: S IS A
Loop 5:  BLOB
Loop 6: TEST.
```

### Дивіться також

-   [db2bindparam()](function.db2-bind-param.html) - Зв'язує змінну PHP із параметром SQL-виразу
-   [db2exec()](function.db2-exec.html) - Виконує SQL-запит безпосередньо
-   [db2execute()](function.db2-execute.html) - Виконує підготовлений SQL-запит
-   [db2fetchrow()](function.db2-fetch-row.html) - Встановлює вказівник набору результатів на наступний рядок або запрошений рядок
-   [db2prepare()](function.db2-prepare.html) - готує SQL-запит до виконання
-   [db2result()](function.db2-result.html) - Повертає один стовпець з рядка у наборі результатів
