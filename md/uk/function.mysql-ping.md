---
navigation:
  - function.mysql-pconnect.md: « mysql\_pconnect
  - function.mysql-query.md: mysql\_query »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_ping
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_ping

(PHP 4 >= 4.3.0, PHP 5)

mysql\_ping — Перевіряє з'єднання з сервером та переєднується за потреби

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_ping()](mysqli.ping.md)

### Опис

```methodsynopsis
mysql_ping(resource $link_identifier = NULL): bool
```

Перевіряє, чи з'єднання з сервером працює. Якщо вона втрачена, автоматично робиться спроба переєднання. Ця функція може бути використана у скриптах, які працюють протягом тривалого часу.

> **Зауваження** :
> 
> Автоматичне відновлення стандартного з'єднання відключено у версіях MySQL >= 5.0.3.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає **`true`**, якщо з'єднання в робочому стані та **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**mysql\_ping()\*\*\*\*

```php
<?php
set_time_limit(0);

$conn = mysql_connect('localhost', 'mysqluser', 'mypass');
$db   = mysql_select_db('mydb');

/* Подразумевается что этот запрос будет выполняться достаточно долго */
$result = mysql_query($sql);
if (!$result) {
    echo 'Запрос #1 не удался, выходим.';
    exit;
}

/* Проверяем что соединение ещё работает, если нет, соединяемся заново */
if (!mysql_ping($conn)) {
    echo 'Соединение потеряно, выходим после запроса #1';
    exit;
}
mysql_free_result($result);

/* Соединение ещё работает, выполняем ещё один запрос */
$result2 = mysql_query($sql2);
?>
```

### Дивіться також

-   [mysql\_thread\_id()](function.mysql-thread-id.md) \- Повертає ідентифікатор потоку
-   [mysql\_list\_processes()](function.mysql-list-processes.md) \- Повертає список процесів MySQL
