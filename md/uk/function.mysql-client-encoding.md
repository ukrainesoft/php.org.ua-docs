---
navigation:
  - function.mysql-affected-rows.md: « mysqlaffectedrows
  - function.mysql-close.md: mysqlclose »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlclientencoding
---
# mysqlclientencoding

(PHP 4> = 4.3.0, PHP 5)

mysqlclientencoding — Повертає кодування з'єднання

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlicharactersetname()](mysqli.character-set-name.md)

### Опис

```methodsynopsis
mysql_client_encoding(resource $link_identifier = NULL): string
```

Повертає значення змінної MySQL `character_set`

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає кодування для цього з'єднання за промовчанням.

### Приклади

**Приклад #1 Приклад використання **mysqlclientencoding()****

```php
<?php
$link    = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$charset = mysql_client_encoding($link);

echo "Текущая кодировка: $charset\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Текущая кодировка: latin1
```

### Дивіться також

-   [mysqlsetcharset()](function.mysql-set-charset.md) - Встановлює кодування клієнта
-   [mysqlrealescapestring()](function.mysql-real-escape-string.md) - Екранує спеціальні символи у рядках для використання у виразах SQL
