---
navigation:
  - function.db2-last-insert-id.md: « db2\_last\_insert\_id
  - function.db2-next-result.md: db2\_next\_result »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_lob\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_lob\_read

(PECL ibm\_db2 >= 1.6.0)

db2\_lob\_read — Отримує певний користувачем розмір LOB-файлів під час кожного виклику

### Опис

```methodsynopsis
db2_lob_read(resource $stmt, int $colnum, int $length): string|false
```

Используйте**db2\_lob\_read()** для ітерації за вказаним стовпцем набору результатів та отримання заданого користувачем розміру LOB-даних.

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

/* Параметры подключения к базе данных */
$db = 'SAMPLE';
$username = 'db2inst1';
$password = 'ibmdb2';

/* Получение ресурса подключения */
$conn = db2_connect($db,$username,$password);

if ($conn) {
    $drop = 'DROP TABLE clob_stream';
    $result = @db2_exec( $conn, $drop );

    $create = 'CREATE TABLE clob_stream (id INTEGER, my_clob CLOB)';
    $result = db2_exec( $conn, $create );

    $variable = "";
    $stmt = db2_prepare($conn, "INSERT INTO clob_stream (id,my_clob) VALUES (1, ?)");
    $variable = "THIS IS A CLOB TEST. THIS IS A CLOB TEST.";
    db2_bind_param($stmt, 1, "variable", DB2_PARAM_IN);
    db2_execute($stmt);

    $sql = "SELECT id,my_clob FROM clob_stream";
    $result = db2_prepare($conn, $sql);
    db2_execute($result);
    db2_fetch_row($result);
    $i = 0;
    /* Чтение LOB-данных */
    while ($data = db2_lob_read($result, 2, 6)) {
        echo "Loop $i: $data\n";
        $i = $i + 1;
    }

    $drop = 'DROP TABLE blob_stream';
    $result = @db2_exec( $conn, $drop );

    $create = 'CREATE TABLE blob_stream (id INTEGER, my_blob CLOB)';
    $result = db2_exec( $conn, $create );

    $variable = "";
    $stmt = db2_prepare($conn, "INSERT INTO blob_stream (id,my_blob) VALUES (1, ?)");
    $variable = "THIS IS A BLOB TEST. THIS IS A BLOB TEST.";
    db2_bind_param($stmt, 1, "variable", DB2_PARAM_IN);
    db2_execute($stmt);

    $sql = "SELECT id,my_blob FROM blob_stream";
    $result = db2_prepare($conn, $sql);
    db2_execute($result);
    db2_fetch_row($result);
    $i = 0;
    /* Чтенеи LOB-данных */
    while ($data = db2_lob_read($result, 2, 6)) {
        echo "Loop $i: $data\n";
        $i = $i + 1;
    }
} else {
    echo 'Нет соединения: ' . db2_conn_errormsg();
}

?>
```

Результат виконання наведеного прикладу:

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

-   [db2\_bind\_param()](function.db2-bind-param.md) \- Зв'язує змінну PHP із параметром SQL-виразу
-   [db2\_exec()](function.db2-exec.md) \- Виконує SQL-запит безпосередньо
-   [db2\_execute()](function.db2-execute.md) \- Виконує підготовлений SQL-запит
-   [db2\_fetch\_row()](function.db2-fetch-row.md) \- Встановлює вказівник набору результатів на наступний рядок або запрошений рядок
-   [db2\_prepare()](function.db2-prepare.md) \- готує SQL-запит до виконання
-   [db2\_result()](function.db2-result.md) \- Повертає один стовпець з рядка у наборі результатів
