Повертає ідентифікатор потоку

-   [« mysqltablename](function.mysql-tablename.html)
    
-   [mysqlunbufferedquery »](function.mysql-unbuffered-query.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Повертає ідентифікатор потоку
    

# mysqlthreadід

(PHP 4> = 4.3.0, PHP 5)

mysqlthreadid — Повертає ідентифікатор потоку.

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqlithreadid()](mysqli.thread-id.html)

### Опис

```methodsynopsis
mysql_thread_id(resource $link_identifier = NULL): int|false
```

**mysqlthreadid()** повертає ідентифікатор потоку. Якщо з'єднання втрачено і ви переєдналися за допомогою [mysqlping()](function.mysql-ping.html)то ідентифікатор потоку зміниться. Це означає, що вам не слід отримувати цей ідентифікатор та зберігати його для подальшого використання. Викликайте функцію тоді, коли вона вам потрібна.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.html) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ідентифікатор потоку у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlthreadid()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$thread_id = mysql_thread_id($link);
if ($thread_id){
    printf("Идентификатор текущего потока: %d\n", $thread_id);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Идентификатор текущего потока: 73
```

### Дивіться також

-   [mysqlping()](function.mysql-ping.html) - Перевіряє з'єднання з сервером та переєднується за потреби
-   [mysqllistprocesses()](function.mysql-list-processes.html) - Повертає список процесів MySQL