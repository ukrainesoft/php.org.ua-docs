Отримання інформації про поточний стан системи

-   [« mysqli::sslset](mysqli.ssl-set.html)
    
-   [mysqli::stmtinit »](mysqli.stmt-init.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Отримання інформації про поточний стан системи
    

# mysqli::stat

# mysqliстати

(PHP 5, PHP 7, PHP 8)

mysqli::stat -- mysqlistat — Отримання інформації про поточний стан системи

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::stat(): string|false
```

Процедурний стиль

```methodsynopsis
mysqli_stat(mysqli $mysql): string|false
```

**mysqliстати()** повертає рядок з інформацією, схожою на ту, що надає команда 'mysqladmin status'. Сюди включається час роботи з моменту завантаження в секундах, кількість запущених процесів, запитів, перезавантажень та відкритих таблиць.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

### Значення, що повертаються

Рядок з інформацією про стан системи . **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::stat()****

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

printf ("Состояние системы: %s\n", $mysqli->stat());

$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

printf("Состояние системы: %s\n", mysqli_stat($link));

mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Состояние системы: Uptime: 272  Threads: 1  Questions: 5340  Slow queries: 0
Opens: 13  Flush tables: 1  Open tables: 0  Queries per second avg: 19.632
Memory in use: 8496K  Max memory used: 8560K
```

### Дивіться також

-   [mysqligetserverinfo()](mysqli.get-server-info.html) - Повертає версію MySQL сервера