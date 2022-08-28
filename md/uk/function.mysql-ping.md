Перевіряє з'єднання з сервером та переєднується за потреби

-   [« mysql\_pconnect](function.mysql-pconnect.html)
    
-   [mysql\_query »](function.mysql-query.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Перевіряє з'єднання з сервером та переєднується за потреби
    

# mysqlping

(PHP 4> = 4.3.0, PHP 5)

mysqlping — Перевіряє з'єднання з сервером та переєднується за потреби

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDO\_MySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqli\_ping()](mysqli.ping.html)

### Опис

```methodsynopsis
mysql_ping(resource $link_identifier = NULL): bool
```

Перевіряє, чи з'єднання з сервером працює. Якщо вона втрачена, автоматично робиться спроба переєднання. Ця функція може бути використана у скриптах, які працюють протягом тривалого часу.

> **Зауваження**
> 
> Автоматичне відновлення стандартного з'єднання відключено у версіях MySQL >= 5.0.3.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`**, якщо з'єднання в робочому стані та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **mysqlping()****

```php
<?php
set_time_limit(0);

$conn = mysql_connect('localhost', 'mysqluser', 'mypass');
$db   = mysql_select_db('mydb');

/* Подразумевается что этот запрос будет выполняться достаточно долго */
$result = mysql_query($sql);
if (!$result) {
    echo 'Запрос #1 не удался, выходим.';
    exit;
}

/* Проверяем что соединение ещё работает, если нет, соединяемся заново */
if (!mysql_ping($conn)) {
    echo 'Соединение потеряно, выходим после запроса #1';
    exit;
}
mysql_free_result($result);

/* Соединение ещё работает, выполняем ещё один запрос */
$result2 = mysql_query($sql2);
?>
```

### Дивіться також

-   [mysql\_thread\_id()](function.mysql-thread-id.html) - Повертає ідентифікатор потоку
-   [mysql\_list\_processes()](function.mysql-list-processes.html) - Повертає список процесів MySQL