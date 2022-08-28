Повертає інформацію про сервер MySQL

-   [« mysql\_get\_proto\_info](function.mysql-get-proto-info.html)
    
-   [mysql\_info »](function.mysql-info.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає інформацію про сервер MySQL
    

# mysqlgetserverinfo

(PHP 4> = 4.0.5, PHP 5)

mysqlgetserverinfo — Повертає інформацію про сервер MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_get\_server\_info()](mysqli.get-server-info.html)
-   [PDO::getAttribute(PDO::ATTR\_SERVER\_VERSION)](pdo.getattribute.html)

### Опис

```methodsynopsis
mysql_get_server_info(resource $link_identifier = NULL): string|false
```

Повертає версію MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає версію сервера MySQL у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlgetserverinfo()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
printf("Версия сервера MySQL: %s\n", mysql_get_server_info());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Версия сервера MySQL: 4.0.1-alpha
```

### Дивіться також

-   [mysql\_get\_client\_info()](function.mysql-get-client-info.html) - Повертає дані про MySQL-клієнт
-   [mysql\_get\_host\_info()](function.mysql-get-host-info.html) - Повертає інформацію про з'єднання з MySQL
-   [mysql\_get\_proto\_info()](function.mysql-get-proto-info.html) - Повертає інформацію про протокол MySQL
-   [phpversion()](function.phpversion.html) - Отримує поточну версію PHP