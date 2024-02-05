---
navigation:
  - function.mysql-field-type.md: « mysql\_field\_type
  - function.mysql-get-client-info.md: mysql\_get\_client\_info »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_free\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_free\_result

(PHP 4, PHP 5)

mysql\_free\_result — Звільняє пам'ять від результату запиту

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_free\_result()](mysqli-result.free.md)
-   Присвоєння значення\*\*`null`\*\*змінної PDO об'єкта, або[PDOStatement::closeCursor()](pdostatement.closecursor.md)

### Опис

```methodsynopsis
mysql_free_result(resource $result): bool
```

**mysql\_free\_result()** звільнить всю пам'ять, яку займає результат, на який посилається переданий дескриптор `result`

**mysql\_free\_result()** потребує виклику тільки в тому випадку, якщо ви серйозно занепокоєні тим, скільки пам'яті використовують ваші запити до БД, які повертають велику кількість даних. Вся пам'ять, що використовується для зберігання цих даних, автоматично очиститься в кінці роботи скрипта.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Якщо як параметр `result` передано не ресурс, то буде викликана помилка рівня E\_WARNING. Варто також зауважити, що [mysql\_query()](function.mysql-query.md) повертає resource лише для запитів SELECT, SHOW, EXPLAIN та DESCRIBE.

### Приклади

**Приклад #1 Приклад використання** mysql\_free\_result()\*\*\*\*

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Не удалось выполнить запрос: ' . mysql_error();
    exit;
}
/* Используем результат, подразумевая, что после этого он нам больше не нужен */
$row = mysql_fetch_assoc($result);

/* Теперь освобождаем результат и продолжаем дальнейшую работу над нашим скриптом */
mysql_free_result($result);

echo $row['id'];
echo $row['email'];
?>
```

### Примітки

> **Зауваження** :
> 
> Для зворотної сумісності може бути використаний наступний застарілий псевдонім: **mysql\_freeresult()**

### Дивіться також

-   [mysql\_query()](function.mysql-query.md) \- Надсилає запит MySQL
-   [is\_resource()](function.is-resource.md) \- Перевіряє, чи є змінна ресурс
