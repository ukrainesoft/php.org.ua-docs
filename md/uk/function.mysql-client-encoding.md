---
navigation:
  - function.mysql-affected-rows.md: « mysql\_affected\_rows
  - function.mysql-close.md: mysql\_close »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_client\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_client\_encoding

(PHP 4 >= 4.3.0, PHP 5)

mysql\_client\_encoding — Повертає кодування з'єднання

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_character\_set\_name()](mysqli.character-set-name.md)

### Опис

```methodsynopsis
mysql_client_encoding(resource $link_identifier = NULL): string
```

Повертає значення змінної MySQL `character_set`

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає кодування для цього з'єднання за промовчанням.

### Приклади

**Приклад #1 Приклад використання** mysql\_client\_encoding()\*\*\*\*

```php
<?php
$link    = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$charset = mysql_client_encoding($link);

echo "Текущая кодировка: $charset\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Текущая кодировка: latin1
```

### Дивіться також

-   [mysql\_set\_charset()](function.mysql-set-charset.md) \- Встановлює кодування клієнта
-   [mysql\_real\_escape\_string()](function.mysql-real-escape-string.md) \- Екранує спеціальні символи у рядках для використання у виразах SQL
