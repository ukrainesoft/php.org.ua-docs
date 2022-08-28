Закриває раніше відкрите з'єднання з базою даних

-   [« mysqli::character\_set\_name](mysqli.character-set-name.html)
    
-   [mysqli::commit »](mysqli.commit.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Закриває раніше відкрите з'єднання з базою даних
    

# mysqli::close

# mysqliclose

(PHP 5, PHP 7, PHP 8)

mysqli::close -- mysqliclose — Закриває раніше відкрите з'єднання з базою даних

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::close(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_close(mysqli $mysql): bool
```

Закриває відкрите з'єднання з базою даних.

Відкриті непостійні з'єднання MySQL та набори результатів автоматично закриваються під час знищення їх об'єктів. Явне закриття відкритих з'єднань та звільнення наборів результатів не є обов'язковим. Однак, рекомендується закрити з'єднання, як тільки скрипт завершить виконання всіх своїх операцій з базою даних, якщо йому ще належить велика обробка після отримання результатів.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::close()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

/* Закройте соединение, как только оно становится ненужным */
$mysqli->close();

foreach ($result as $row) {
    /* Обработка данных, полученных из базы данных */
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($mysqli, "SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

/* Закройте соединение, как только оно становится ненужным */
mysqli_close($mysqli);

foreach ($result as $row) {
    /* Обработка данных, полученных из базы данных */
}
```

### Примітки

> **Зауваження**
> 
> **mysqliclose()** не закриває постійні з'єднання. Для отримання подробиць дивіться посібник з [persistent connections](features.persistent-connections.html)

### Дивіться також

-   [mysqli::\_\_construct()](mysqli.construct.html) - Встановлює нове з'єднання із сервером MySQL
-   [mysqli\_init()](mysqli.init.html) - Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()
-   [mysqli\_real\_connect()](mysqli.real-connect.html) - Встановлює з'єднання із сервером mysql
-   [mysqli\_free\_result()](mysqli-result.free.html) - звільняє пам'ять, зайняту результатами запиту