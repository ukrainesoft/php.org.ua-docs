Оновлення

-   [« mysqli::reapasyncquery](mysqli.reap-async-query.html)
    
-   [mysqli::releasesavepoint »](mysqli.release-savepoint.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Оновлення
    

# mysqli::refresh

# mysqlirefresh

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqli::refresh -- mysqlirefresh — Оновлення

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::refresh(int $flags): bool
```

Процедурний стиль

```methodsynopsis
mysqli_refresh(mysqli $mysql, int $flags): bool
```

Очищає таблиці або кеш або скидає копію серверної інформації.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

`flags`

Налаштування оновлення задаються константами MYSQLIREFRESH, які описані у розділі документації [Константы MySQLi](mysqli.constants.html)

Дивіться також офіційну документацію [» MySQL Refresh](http://dev.mysql.com/doc/mysql/en/mysql-refresh.html)

### Значення, що повертаються

**`true`** у разі успішного виконання, **`false`** в іншому випадку.

### Дивіться також

-   [mysqlipoll()](mysqli.poll.html) - Опитування підключень