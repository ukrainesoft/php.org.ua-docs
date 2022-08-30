Встановлює режим звіту про помилки mysqli

-   [« mysqlidriver::embeddedserverstart](mysqli-driver.embedded-server-start.html)
    
-   [mysqliwarning »](class.mysqli-warning.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlidriver](class.mysqli-driver.html)
    
-   Встановлює режим звіту про помилки mysqli
    

# mysqlidriver::$reportmode

# mysqlireport

(PHP 5, PHP 7, PHP 8)

mysqlidriver::$reportmode - mysqlireport — Встановлює режим звіту про помилки mysqli

### Опис

Об'єктно-орієнтований стиль

int [$mysqlidriver->reportmode](mysqli-driver.report-mode.html)

Процедурний стиль

```methodsynopsis
mysqli_report(int $flags): bool
```

Залежно від прапорів, функція встановлює режим звіту про помилки mysqli на виключення, попередження чи відсутність. Якщо встановлено значення **`MYSQLI_REPORT_ALL`** або **`MYSQLI_REPORT_INDEX`**, функція також інформуватиме про запити, які не використовують індекс (або використовують неправильний індекс).

Починаючи з PHP 8.1.0, за замовчуванням встановлено значення `MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT`. Раніше воно було **`MYSQLI_REPORT_OFF`**

### Список параметрів

`flags`

**Прапори, що підтримуються**

| Имя                        | Описание                                                                                                           |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **`MYSQLI_REPORT_OFF`**    | Вимкнути протоколювання                                                                                            |
| **`MYSQLI_REPORT_ERROR`**  | Заносити до протоколу помилки викликів функцій mysqli                                                              |
| **`MYSQLI_REPORT_STRICT`** | Замість повідомлень про помилки викидати виняток [mysqlisqlexception](class.mysqli-sql-exception.html)             |
| **`MYSQLI_REPORT_INDEX`**  | Заносити до протоколу факти використання у запитах невірного індексу (або коли індекс не використовується взагалі) |
| **`MYSQLI_REPORT_ALL`**    | Увімкнути всі налаштування (заносити до протоколу всі події)                                                       |

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер за замовчуванням встановлено значення \`MYSQLI\_REPORT\_ERROR |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

/* включение протоколирования */
$driver = new mysqli_driver();
$driver->report_mode = MYSQLI_REPORT_ALL;

try {
    /* если получится подключится, будет выброшено исключение mysqli_sql_exception */
    $mysqli = new mysqli("localhost", "my_user", "my_password", "my_db");

    /* этот запрос должен сообщить об ошибке */
    $result = $mysqli->query("SELECT Name FROM Nonexistingtable WHERE population > 50000");

    /* этот запрос должен сообщить о неверном индексе, если у столбца population нет индекса */
    $result = $mysqli->query("SELECT Name FROM City WHERE population > 50000");
} catch (mysqli_sql_exception $e) {
    error_log($e->__toString());
}
```

**Приклад #2 Процедурний стиль**

```php
<?php

/* включение протоколирования */
mysqli_report(MYSQLI_REPORT_ALL);

try {
    /* Если соединение завершилось с ошибкой, будет выброшено исключение mysqli_sql_exception */
    $link = mysqli_connect("localhost", "my_user", "my_password", "my_db");

    /* этот запрос должен сообщить об ошибке */
    $result = mysqli_query($link, "SELECT Name FROM Nonexistingtable WHERE population > 50000");

    /* этот запрос должен сообщить о неверном индексе, если у столбца population нет индекса */
    $result = mysqli_query($link, "SELECT Name FROM City WHERE population > 50000");
} catch (mysqli_sql_exception $e) {
    error_log($e->__toString());
}
```

**Приклад #3 Звіт про помилки, крім помилок неправильного індексу**

```php
<?php

/* включение протоколирования */
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);

try {
    /* если получится подключится, будет выброшено исключение mysqli_sql_exception */
    $mysqli = new mysqli("localhost", "my_user", "my_password", "my_db");

    /* этот запрос должен сообщить об ошибке */
    $result = $mysqli->query("SELECT Name FROM Nonexistingtable WHERE population > 50000");

    /* это НЕ БУДЕТ сообщать об ошибках, даже если индекс недоступен */
    $result = $mysqli->query("SELECT Name FROM City WHERE population > 50000");
} catch (mysqli_sql_exception $e) {
    error_log($e->__toString());
}
```

### Дивіться також

-   [mysqlisqlexception](class.mysqli-sql-exception.html)
-   [setexceptionhandler()](function.set-exception-handler.html) - Задає користувальницький обробник винятків
-   [errorreporting()](function.error-reporting.html) - Задає, які помилки PHP потраплять у звіт