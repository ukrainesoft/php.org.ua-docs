---
navigation:
  - mysqli.autocommit.md: '« mysqli::autocommit'
  - mysqli.change-user.md: 'mysqli::changeuser »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::begintransaction'
---
# mysqli::begintransaction

# mysqlibegintransaction

(PHP 5> = 5.5.0, PHP 7, PHP 8)

mysqli::begintransaction - mysqlibegintransaction - Стартує транзакцію

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::begin_transaction(int $flags = 0, ?string $name = null): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_begin_transaction(mysqli $mysql, int $flags = 0, ?string $name = null): bool
```

Стартує транзакцію. Потрібно InnoDB (дозволено за замовчуванням). Для додаткової інформації, як працюють транзакції у MySQL, читайте [» http://dev.mysql.com/doc/mysql/en/commit.html](http://dev.mysql.com/doc/mysql/en/commit.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

`flags`

Коректні прапори:

-   **`MYSQLI_TRANS_START_READ_ONLY`**: Стартувати транзакцію як "START TRANSACTION READ ONLY" Потрібно MySQL 5.6 або вище.
    
-   **`MYSQLI_TRANS_START_READ_WRITE`**: Стартувати транзакцію як "START TRANSACTION READ WRITE" Потрібно MySQL 5.6 або вище.
    
-   **`MYSQLI_TRANS_START_WITH_CONSISTENT_SNAPSHOT`**: Стартувати транзакцію як "START TRANSACTION WITH CONSISTENT SNAPSHOT"
    

`name`

Крапка збереження транзакції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `name` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **mysqli::begintransaction()****

Об'єктно-орієнтований стиль

```php
<?php

/* Указать mysqli выбрасывать исключение в случае возникновения ошибки */
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);

$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Движок таблиц должен поддерживать транзакции */
$mysqli->query("CREATE TABLE IF NOT EXISTS language (
    Code text NOT NULL,
    Speakers int(11) NOT NULL
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;");

/* Начало транзакции */
$mysqli->begin_transaction();

try {
    /* Добавление каких-то значений */
    $mysqli->query("INSERT INTO language(Code, Speakers) VALUES ('DE', 42000123)");

    /* Попытка добавить недопустимые значения */
    $language_code = 'FR';
    $native_speakers = 'Unknown';
    $stmt = $mysqli->prepare('INSERT INTO language(Code, Speakers) VALUES (?,?)');
    $stmt->bind_param('ss', $language_code, $native_speakers);
    $stmt->execute();

    /* Если код достигает этой точки без ошибок, фиксируем данные в базе данных. */
    $mysqli->commit();
} catch (mysqli_sql_exception $exception) {
    $mysqli->rollback();

    throw $exception;
}
```

Процедурний стиль

```php
<?php

/* Указать mysqli выбрасывать исключение в случае возникновения ошибки */
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);

$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Движок таблиц должен поддерживать транзакции */
mysqli_query($mysqli, "CREATE TABLE IF NOT EXISTS language (
    Code text NOT NULL,
    Speakers int(11) NOT NULL
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;");

/* Начало транзакции */
mysqli_begin_transaction($mysqli);

try {
    /* Добавление каких-то значений */
    mysqli_query($mysqli, "INSERT INTO language(Code, Speakers) VALUES ('DE', 42000123)");

    /* Попытка добавить недопустимые значения */
    $language_code = 'FR';
    $native_speakers = 'Unknown';
    $stmt = mysqli_prepare($mysqli, 'INSERT INTO language(Code, Speakers) VALUES (?,?)');
    mysqli_stmt_bind_param($stmt, 'ss', $language_code, $native_speakers);
    mysqli_stmt_execute($stmt);

    /* Если код достигает этой точки без ошибок, фиксируем данные в базе данных. */
    mysqli_commit($mysqli);
} catch (mysqli_sql_exception $exception) {
    mysqli_rollback($mysqli);

    throw $exception;
}
```

### Примітки

> **Зауваження**
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqliautocommit()](mysqli.autocommit.md) - Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqlicommit()](mysqli.commit.md) - Фіксує поточну транзакцію
-   [mysqlirollback()](mysqli.rollback.md) - Відкат поточної транзакції
