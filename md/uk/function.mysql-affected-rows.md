---
navigation:
  - ref.mysql.md: « MySQL
  - function.mysql-client-encoding.md: mysqlclientencoding »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlaffectedrows
---
# mysqlaffectedrows

(PHP 4, PHP 5)

mysqlaffectedrows - Повертає число порушених минулою операцією рядів

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqliaffectedrows()](mysqli.affected-rows.md)
-   [PDOStatement::rowCount()](pdostatement.rowcount.md)

### Опис

```methodsynopsis
mysql_affected_rows(resource $link_identifier = NULL): int
```

Повертає кількість рядів, які торкнулися останнім INSERT, UPDATE, REPLACE або DELETE запитом, пов'язаним з дескриптором `link_identifier`

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає кількість змінених записів у разі успішного виконання, і -1 якщо останній запит не вдався.

Якщо останній запит був DELETE без вказівки WHERE і, відповідно, таблицю було очищено, функція поверне нуль у всіх версіях MySQL до 4.1.2.

При використанні UPDATE MySQL не оновить колонки, що вже містять нове значення. Внаслідок цього, функція **mysqlaffectedrows()** не завжди повертає кількість рядів, що підійшли під умови, лише кількість рядів, оновлених запитом.

Запит REPLACE спочатку видаляє запис із зазначеним первинним ключем, а потім вставляє новий. Ця функція повертає кількість видалених записів разом із кількістю вставлених.

У разі використання запитів типу "INSERT ... ON DUPLICATE KEY UPDATE", значення, що повертається, буде дорівнює `1` у випадку, якщо була зроблена вставка, або `2` при оновленні існуючого ряду.

### Приклади

**Приклад #1 Приклад використання **mysqlaffectedrows()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
mysql_select_db('mydb');

/* здесь функция вернёт корректное число удалённых записей */
mysql_query('DELETE FROM mytable WHERE id < 10');
printf("Удалено записей: %d\n", mysql_affected_rows());

/* если WHERE всегда возвращает false, то функция возвращает 0 */
mysql_query('DELETE FROM mytable WHERE 0');
printf("Удалено записей: %d\n", mysql_affected_rows());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Удалено записей: 10
Удалено записей: 0
```

**Приклад #2 Приклад використання **mysqlaffectedrows()** з транзакціями**

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
mysql_select_db('mydb');

/* Обновляем ряды */
mysql_query("UPDATE mytable SET used=1 WHERE id < 10");
printf ("Обновлено записей: %d\n", mysql_affected_rows());
mysql_query("COMMIT");
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Обновлено записей: 10
```

### Примітки

> **Зауваження** **Транзакції**
> 
> При використанні транзакцій **mysqlaffectedrows()** потрібно викликати після запитів INSERT, UPDATE, DELETE, але з COMMIT.

> **Зауваження** **Запити SELECT**
> 
> Щоб отримати кількість рядів, повернутих SELECT-запитом, використовуйте функцію [mysqlnumrows()](function.mysql-num-rows.md)

> **Зауваження** **Каскадні зовнішні ключі**
> 
> **mysqlaffectedrows()** не підраховує ряди, неявно змінені обмеженнями ON DELETE CASCADE та/або ON UPDATE CASCADE.

### Дивіться також

-   [mysqlnumrows()](function.mysql-num-rows.md) - Повертає кількість рядів результату запиту
-   [mysqlinfo()](function.mysql-info.md) - Повертає інформацію про останній запит
