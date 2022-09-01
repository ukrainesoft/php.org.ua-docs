---
navigation:
  - mysqli.character-set-name.html: '« mysqli::charactersetname'
  - mysqli.commit.md: 'mysqli::commit »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::close'
---
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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

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
> **mysqliclose()** не закриває постійні з'єднання. Для отримання подробиць дивіться посібник з [persistent connections](features.persistent-connections.md)

### Дивіться також

-   [mysqli::construct()](mysqli.construct.md) - Встановлює нове з'єднання із сервером MySQL
-   [mysqliinit()](mysqli.init.md) - Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()
-   [mysqlirealconnect()](mysqli.real-connect.md) - Встановлює з'єднання із сервером mysql
-   [mysqlifreeresult()](mysqli-result.free.md) - звільняє пам'ять, зайняту результатами запиту
