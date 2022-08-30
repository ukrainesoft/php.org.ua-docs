Екранує спеціальні символи в рядках для використання у виразах SQL

-   [« mysqlquery](function.mysql-query.html)
    
-   [mysqlresult »](function.mysql-result.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Екранує спеціальні символи в рядках для використання у виразах SQL
    

# mysqlrealescapestring

(PHP 4> = 4.3.0, PHP 5)

mysqlrealescapestring — Екран спеціальних символів у рядках для використання у виразах SQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlirealescapestring()](mysqli.real-escape-string.html)
-   [PDO::quote()](pdo.quote.html)

### Опис

```methodsynopsis
mysql_real_escape_string(string $unescaped_string, resource $link_identifier = NULL): string
```

Екранує спеціальні символи в `unescaped_string`, беручи до уваги кодування з'єднання, таким чином, що результат можна безпечно використовувати в SQL-запиті у функції [mysqlquery()](function.mysql-query.html). Якщо вставляються бінарні дані, то до них необхідно застосовувати цю функцію.

**mysqlrealescapestring()** викликає бібліотечну функцію MySQL mysqlrealescapestring, яка додає зворотну косу рису до наступних символів: `\x00` `\n` `\r` `\` `'` `"` і `\x1a`

Ця функція повинна завжди (за декількома винятками) використовуватися для того, щоб убезпечити дані, що вставляють у запит перед відправкою його до MySQL.

**Застереження**

# Безпека: кодування символів за промовчанням

Кодування символів має встановлюватися як на сервері, так і за допомогою функції [mysqlsetcharset()](function.mysql-set-charset.html), щоб впливати на поведінку **mysqlrealescapestring()**. Докладніше описано в розділі [кодування символів](mysqlinfo.concepts.charset.html)

### Список параметрів

`unescaped_string`

Рядок, що екранується.

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок, де екрановані всі необхідні символи, або **`false`** у разі виникнення помилки.

### Помилки

Запуск цієї функції без існуючого з'єднання з MySQL викликає помилку рівня **`E_WARNING`**. Цю функцію можна запускати лише якщо є з'єднання з MySQL.

### Приклади

**Приклад #1 Простий приклад використання **mysqlrealescapestring()****

```php
<?php
// Соединение
$link = mysql_connect('mysql_host', 'mysql_user', 'mysql_password')
    OR die(mysql_error());

// Запрос
$query = sprintf("SELECT * FROM users WHERE user='%s' AND password='%s'",
            mysql_real_escape_string($user),
            mysql_real_escape_string($password));
?>
```

**Приклад #2 Приклад використання **mysqlrealescapestring()** без наявності з'єднання**

Цей приклад показує, що станеться, якщо викликати цю функцію без з'єднання з MySQL.

```php
<?php
// Коннекта к MySQL нет

$lastname  = "O'Reilly";
$_lastname = mysql_real_escape_string($lastname);

$query = "SELECT * FROM actors WHERE last_name = '$_lastname'";

var_dump($_lastname);
var_dump($query);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Warning: mysql_real_escape_string(): No such file or directory in /this/test/script.php on line 5
Warning: mysql_real_escape_string(): A link to the server could not be established in /this/test/script.php on line 5

bool(false)
string(41) "SELECT * FROM actors WHERE last_name = ''"
```

**Приклад #3 Приклад злому з використанням ін'єкції SQL.**

```php
<?php
// Мы никак не проверили переменную $_POST['password'],
// а она может содержать совсем не то, что мы ожидали. Например:
$_POST['username'] = 'aidan';
$_POST['password'] = "' OR ''='";

// посылаем запрос, чтобы проверить имя и пароль пользователя
$query = "SELECT * FROM users WHERE user='{$_POST['username']}' AND password='{$_POST['password']}'";
mysql_query($query);

// посмотрим, какой запрос будет отправлен в MySQL:
echo $query;
?>
```

Запит, який буде надіслано MySQL:

```
SELECT * FROM users WHERE user='aidan' AND password='' OR ''=''
```

Це дозволить будь-кому увійти в систему без пароля.

### Примітки

> **Зауваження**
> 
> функцію **mysqlrealescapestring()** можна використовувати тільки після встановлення з'єднання з MySQL. В іншому випадку виникне помилка рівня **`E_WARNING`**, а функція поверне **`false`**. Якщо `link_identifier` не вказано, використовується останнє відкрите з'єднання.

> **Зауваження**
> 
> Якщо [magicquotesgpc](info.configuration.html#ini.magic-quotes-gpc) включені, то спочатку дані слід обробити функцією [stripslashes()](function.stripslashes.html). Якщо цю функцію застосувати до вже проекранованих даних, дані будуть проекрановані двічі.

> **Зауваження**
> 
> Якщо не користуватися цією функцією, то запит стає вразливим для [взлома с помощью SQL-инъекций](security.database.sql-injection.html)

> **Зауваження** **mysqlrealescapestring()** не екранує символи `%` і `_`. Ці символи є масками груп символів в операторах MySQL `LIKE` `GRANT` і `REVOKE`

### Дивіться також

-   [mysqlsetcharset()](function.mysql-set-charset.html) - Встановлює кодування клієнта
-   [mysqlclientencoding()](function.mysql-client-encoding.html) - Повертає кодування з'єднання
-   [addslashes()](function.addslashes.html) - Екранує рядок за допомогою слішів
-   [stripslashes()](function.stripslashes.html) - Видаляє екранування символів
-   Директива [magicquotesgpc](info.configuration.html#ini.magic-quotes-gpc)
-   Директива [magicquotesruntime](info.configuration.html#ini.magic-quotes-runtime)