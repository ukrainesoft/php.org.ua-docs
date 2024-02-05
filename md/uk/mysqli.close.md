---
navigation:
  - mysqli.character-set-name.md: '« mysqli::character\_set\_name'
  - mysqli.commit.md: 'mysqli::commit »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::close

# mysqli\_close

(PHP 5, PHP 7, PHP 8)

mysqli::close -- mysqli\_close — Закриває раніше відкрите з'єднання з базою даних

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::close(): true
```

Процедурний стиль

```methodsynopsis
mysqli_close(mysqli $mysql): true
```

Закриває відкрите з'єднання з базою даних.

Відкриті непостійні з'єднання MySQL та набори результатів автоматично закриваються під час знищення їх об'єктів. Явне закриття відкритих з'єднань та звільнення наборів результатів не є обов'язковим. Однак рекомендується закрити з'єднання, як тільки скрипт завершить виконання всіх своїх операцій з базою даних, якщо йому ще потрібно буде більша обробка після отримання результатів.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер повертає значення **`true`**. . Раніше вона повертала значення \*\*`false`\*\*в случае возникновения ошибки. |

### Приклади

**Пример #1 Пример использования**mysqli::close()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$result = $mysqli->query("SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

/* Закройте соединение, как только оно становится ненужным */
$mysqli->close();

foreach ($result as $row) {
    /* Обработка данных, полученных из базы данных */
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = mysqli_connect("localhost", "my_user", "my_password", "world");

$result = mysqli_query($mysqli, "SELECT Name, CountryCode FROM City ORDER BY ID LIMIT 3");

/* Закройте соединение, как только оно становится ненужным */
mysqli_close($mysqli);

foreach ($result as $row) {
    /* Обработка данных, полученных из базы данных */
}
```

### Примітки

> **Зауваження** :
> 
> **mysqli\_close()** не закриває постійні з'єднання. Для отримання подробиць дивіться посібник з [persistent connections](features.persistent-connections.md)

### Дивіться також

-   [mysqli::\_\_construct()](mysqli.construct.md) \- Встановлює нове з'єднання із сервером MySQL
-   [mysqli\_init()](mysqli.init.md) \- Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqli\_real\_connect()
-   [mysqli\_real\_connect()](mysqli.real-connect.md) \- Встановлює з'єднання із сервером mysql
-   [mysqli\_free\_result()](mysqli-result.free.md) \- звільняє пам'ять, зайняту результатами запиту
