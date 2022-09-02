---
navigation:
  - function.mysql-field-type.md: « mysqlfieldtype
  - function.mysql-get-client-info.md: mysqlgetclientinfo »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlfreeresult
---
# mysqlfreeresult

(PHP 4, PHP 5)

mysqlfreeresult — Звільняє пам'ять від результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlifreeresult()](mysqli-result.free.md)
-   Присвоєння значення **`null`** змінної PDO об'єкта, або [PDOStatement::closeCursor()](pdostatement.closecursor.md)

### Опис

```methodsynopsis
mysql_free_result(resource $result): bool
```

**mysqlfreeresult()** звільнить всю пам'ять, яку займає результат, на який посилається переданий дескриптор `result`

**mysqlfreeresult()** потребує виклику тільки в тому випадку, якщо ви серйозно занепокоєні тим, скільки пам'яті використовують ваші запити до БД, які повертають велику кількість даних. Вся пам'ять, що використовується для зберігання цих даних, автоматично очиститься в кінці роботи скрипта.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Якщо як параметр `result` передано не ресурс, то буде викликана помилка рівня EWARNING. Варто також зауважити, що [mysqlquery()](function.mysql-query.md) повертає resource лише для запитів SELECT, SHOW, EXPLAIN та DESCRIBE.

### Приклади

**Приклад #1 Приклад використання **mysqlfreeresult()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Не удалось выполнить запрос: ' . mysql_error();
    exit;
}
/* Используем результат, подразумевая, что после этого он нам больше не нужен */
$row = mysql_fetch_assoc($result);

/* Теперь освобождаем результат и продолжаем дальнейшую работу над нашим скриптом */
mysql_free_result($result);

echo $row['id'];
echo $row['email'];
?>
```

### Примітки

> **Зауваження**
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysqlfreeresult()**

### Дивіться також

-   [mysqlquery()](function.mysql-query.md) - Надсилає запит MySQL
-   [ісresource()](function.is-resource.md) - Перевіряє, чи є змінна ресурсом
