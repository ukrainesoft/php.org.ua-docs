Повертає кодування з'єднання

-   [« mysql\_affected\_rows](function.mysql-affected-rows.html)
    
-   [mysql\_close »](function.mysql-close.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає кодування з'єднання
    

# mysqlclientencoding

(PHP 4> = 4.3.0, PHP 5)

mysqlclientencoding — Повертає кодування з'єднання

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_character\_set\_name()](mysqli.character-set-name.html)

### Опис

```methodsynopsis
mysql_client_encoding(resource $link_identifier = NULL): string
```

Повертає значення змінної MySQL `character_set`

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

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

-   [mysql\_set\_charset()](function.mysql-set-charset.html) - Встановлює кодування клієнта
-   [mysql\_real\_escape\_string()](function.mysql-real-escape-string.html) - Екранує спеціальні символи у рядках для використання у виразах SQL