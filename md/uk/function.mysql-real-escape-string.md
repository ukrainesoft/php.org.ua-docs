---
navigation:
  - function.mysql-query.md: « mysql\_query
  - function.mysql-result.md: mysql\_result »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_real\_escape\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_real\_escape\_string

(PHP 4 >= 4.3.0, PHP 5)

mysql\_real\_escape\_string — Екран спеціальних символів у рядках для використання у виразах SQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_real\_escape\_string()](mysqli.real-escape-string.md)
-   [PDO::quote()](pdo.quote.md)

### Опис

```methodsynopsis
mysql_real_escape_string(string $unescaped_string, resource $link_identifier = NULL): string
```

Екранує спеціальні символи в `unescaped_string`, беручи до уваги кодування з'єднання, таким чином, що результат можна безпечно використовувати в SQL-запиті у функції [mysql\_query()](function.mysql-query.md). Якщо вставляються бінарні дані, то до них необхідно застосовувати цю функцію.

**mysql\_real\_escape\_string()** викликає бібліотечну функцію MySQL mysql\_real\_escape\_string, яка додає зворотну косу рису до наступних символів: `\x00` `\n` `\r` `\` `'` `"`и`\x1a`

Ця функція повинна завжди (за декількома винятками) використовуватися для того, щоб убезпечити дані, що вставляють у запит перед відправкою його до MySQL.

**Застереження**

# Безпека: кодування символів за промовчанням

Кодування символів має встановлюватися як на сервері, так і за допомогою функції [mysql\_set\_charset()](function.mysql-set-charset.md), щоб впливати на поведінку **mysql\_real\_escape\_string()**. Докладніше описано в розділі [кодування символів](mysqlinfo.concepts.charset.md)

### Список параметрів

`unescaped_string`

Рядок, що екранується.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок, де екрановані всі необхідні символи, або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Запуск цієї функції без існуючого з'єднання з MySQL викликає помилку рівня **`E_WARNING`**. Цю функцію можна запускати лише якщо є з'єднання з MySQL.

### Приклади

**Приклад #1 Простий приклад використання **mysql\_real\_escape\_string()****

```php
<?php
// Соединение
$link = mysql_connect('mysql_host', 'mysql_user', 'mysql_password')
    OR die(mysql_error());

// Запрос
$query = sprintf("SELECT * FROM users WHERE user='%s' AND password='%s'",
            mysql_real_escape_string($user),
            mysql_real_escape_string($password));
?>
```

**Приклад #2 Приклад використання** mysql\_real\_escape\_string()\*\* без наявності з'єднання\*\*

Цей приклад показує, що станеться, якщо викликати цю функцію без з'єднання з MySQL.

```php
<?php
// Коннекта к MySQL нет

$lastname  = "O'Reilly";
$_lastname = mysql_real_escape_string($lastname);

$query = "SELECT * FROM actors WHERE last_name = '$_lastname'";

var_dump($_lastname);
var_dump($query);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Warning: mysql_real_escape_string(): No such file or directory in /this/test/script.php on line 5
Warning: mysql_real_escape_string(): A link to the server could not be established in /this/test/script.php on line 5

bool(false)
string(41) "SELECT * FROM actors WHERE last_name = ''"
```

**Приклад #3 Приклад злому з використанням ін'єкції SQL.**

```php
<?php
// Мы никак не проверили переменную $_POST['password'],
// а она может содержать совсем не то, что мы ожидали. НаПриклад:
$_POST['username'] = 'aidan';
$_POST['password'] = "' OR ''='";

// посылаем запрос, чтобы проверить имя и пароль пользователя
$query = "SELECT * FROM users WHERE user='{$_POST['username']}' AND password='{$_POST['password']}'";
mysql_query($query);

// посмотрим, какой запрос будет отправлен в MySQL:
echo $query;
?>
```

Запит, який буде надіслано MySQL:

```
SELECT * FROM users WHERE user='aidan' AND password='' OR ''=''
```

Це дозволить будь-кому увійти в систему без пароля.

### Примітки

> **Зауваження** :
> 
> Функцию**mysql\_real\_escape\_string()** можна використовувати тільки після встановлення з'єднання з MySQL. В іншому випадку виникне помилка рівня **`E_WARNING`**, а функція поверне **`false`**. Якщо `link_identifier` не вказано, використовується останнє відкрите з'єднання.

> **Зауваження** :
> 
> Якщо не користуватися цією функцією, то запит стає вразливим для [злому за допомогою SQL-ін'єкцій](security.database.sql-injection.md)

> **Зауваження** **mysql\_real\_escape\_string()** не екранує символи `%`и`_`. Ці символи є масками груп символів в операторах MySQL `LIKE` `GRANT`и`REVOKE`

### Дивіться також

-   [mysql\_set\_charset()](function.mysql-set-charset.md) \- Встановлює кодування клієнта
-   [mysql\_client\_encoding()](function.mysql-client-encoding.md) \- Повертає кодування з'єднання
