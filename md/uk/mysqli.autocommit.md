Вмикає або вимикає автоматичну фіксацію змін бази даних

-   [« mysqli::$affectedrows](mysqli.affected-rows.html)
    
-   [mysqli::begintransaction »](mysqli.begin-transaction.html)
    
-   [PHP Manual](index.md)
    
-   [mysqli](class.mysqli.md)
    
-   Вмикає або вимикає автоматичну фіксацію змін бази даних
    

# mysqli::autocommit

# mysqliautocommit

(PHP 5, PHP 7, PHP 8)

mysqli::autocommit -- mysqliautocommit — Вмикає або вимикає автоматичну фіксацію змін бази даних

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::autocommit(bool $enable): bool
```

Процедурний стиль

```methodsynopsis
mysqli_autocommit(mysqli $mysql, bool $enable): bool
```

Вмикає або вимикає режим автоматичної фіксації змін для з'єднання з базою даних.

Щоб визначити поточний стан режиму, використовуйте SQL `SELECT @@autocommit`

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

`enable`

Вмикає або вимикає режим автоматичної фіксації змін.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::autocommit()****

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

/* Отключить автоматическую фиксацию */
$mysqli->autocommit(false);

$result = $mysqli->query("SELECT @@autocommit");
$row = $result->fetch_row();
printf("Автоматическая фиксация: %s\n", $row[0]);

try {
    /* Подготовить выражение для добавления */
    $stmt = $mysqli->prepare('INSERT INTO language(Code, Speakers) VALUES (?,?)');
    $stmt->bind_param('ss', $language_code, $native_speakers);

    /* Добавление каких-то значений */
    $language_code = 'DE';
    $native_speakers = 50_123_456;
    $stmt->execute();
    $language_code = 'FR';
    $native_speakers = 40_546_321;
    $stmt->execute();

    /* Зафиксируйте данные в базе данных. Это не устанавливает autocommit=true */
    $mysqli->commit();
    print "Зафиксировано 2 строки в базе данных\n";

    $result = $mysqli->query("SELECT @@autocommit");
    $row = $result->fetch_row();
    printf("Автоматическая фиксация: %s\n", $row[0]);

    /* Попробуйте вставить больше значений */
    $language_code = 'PL';
    $native_speakers = 30_555_444;
    $stmt->execute();
    $language_code = 'DK';
    $native_speakers = 5_222_444;
    $stmt->execute();

    /* Установка autocommit=true вызовет фиксацию */
    $mysqli->autocommit(true);

    print "Зафиксировано 2 строки в базе данных\n";
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

/* Отключить автоматическую фиксацию */
mysqli_autocommit($mysqli, false);

$result = mysqli_query($mysqli, "SELECT @@autocommit");
$row = mysqli_fetch_row($result);
printf("Автоматическая фиксация: %s\n", $row[0]);

try {
    /* Подготовить выражение для добавления */
    $stmt = mysqli_prepare($mysqli, 'INSERT INTO language(Code, Speakers) VALUES (?,?)');
    mysqli_stmt_bind_param($stmt, 'ss', $language_code, $native_speakers);

    /* Добавление каких-то значений */
    $language_code = 'DE';
    $native_speakers = 50_123_456;
    mysqli_stmt_execute($stmt);
    $language_code = 'FR';
    $native_speakers = 40_546_321;
    mysqli_stmt_execute($stmt);

    /* Зафиксируйте данные в базе данных. Это не устанавливает autocommit=true */
    mysqli_commit($mysqli);
    print "Зафиксировано 2 строки в базе данных\n";

    $result = mysqli_query($mysqli, "SELECT @@autocommit");
    $row = mysqli_fetch_row($result);
    printf("Автоматическая фиксация: %s\n", $row[0]);

    /* Попробуйте вставить больше значений */
    $language_code = 'PL';
    $native_speakers = 30_555_444;
    mysqli_stmt_execute($stmt);
    $language_code = 'DK';
    $native_speakers = 5_222_444;
    mysqli_stmt_execute($stmt);

    /* Установка autocommit=true вызовет фиксацию */
    mysqli_autocommit($mysqli, true);

    print "Зафиксировано 2 строки в базе данных\n";
} catch (mysqli_sql_exception $exception) {
    mysqli_rollback($mysqli);

    throw $exception;
}
```

Результат виконання даних прикладів:

```
Автоматическая фиксация: 0
Зафиксировано 2 строки в базе данных
Автоматическая фиксация: 0
Зафиксировано 2 строки в базе данных
Автоматическая фиксация: 0
Зафиксировано 2 строки в базе данных
Автоматическая фиксация: 0
Зафиксировано 2 строки в базе данных
```

### Примітки

> **Зауваження**
> 
> Функція не працює з нетранзакційними типами таблиць (наприклад, MyISAM або ISAM).

### Дивіться також

-   [mysqlibegintransaction()](mysqli.begin-transaction.html) - Стартує транзакцію
-   [mysqlicommit()](mysqli.commit.md) - Фіксує поточну транзакцію
-   [mysqlirollback()](mysqli.rollback.md) - Відкат поточної транзакції