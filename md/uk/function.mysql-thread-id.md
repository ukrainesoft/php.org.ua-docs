---
navigation:
  - function.mysql-tablename.md: « mysql\_tablename
  - function.mysql-unbuffered-query.md: mysql\_unbuffered\_query »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_thread\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_thread\_id

(PHP 4 >= 4.3.0, PHP 5)

mysql\_thread\_id — Повертає ідентифікатор потоку.

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_thread\_id()](mysqli.thread-id.md)

### Опис

```methodsynopsis
mysql_thread_id(resource $link_identifier = NULL): int|false
```

**mysql\_thread\_id()** повертає ідентифікатор потоку. Якщо з'єднання втрачено і ви переєдналися за допомогою [mysql\_ping()](function.mysql-ping.md)то ідентифікатор потоку зміниться. Це означає, що вам не слід отримувати цей ідентифікатор та зберігати його для подальшого використання. Викликайте функцію тоді, коли вона вам потрібна.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Ідентифікатор потоку у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysql\_thread\_id()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
$thread_id = mysql_thread_id($link);
if ($thread_id){
    printf("Идентификатор текущего потока: %d\n", $thread_id);
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Идентификатор текущего потока: 73
```

### Дивіться також

-   [mysql\_ping()](function.mysql-ping.md) \- Перевіряє з'єднання з сервером та переєднується за потреби
-   [mysql\_list\_processes()](function.mysql-list-processes.md) \- Повертає список процесів MySQL
