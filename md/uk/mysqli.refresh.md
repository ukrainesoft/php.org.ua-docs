Оновлення

-   [« mysqli::reap\_async\_query](mysqli.reap-async-query.html)
    
-   [mysqli::release\_savepoint »](mysqli.release-savepoint.html)
    
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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`flags`

Налаштування оновлення задаються константами MYSQLIREFRESH, які описані у розділі документації [Константы MySQLi](mysqli.constants.html)

Дивіться також офіційну документацію [» MySQL Refresh](http://dev.mysql.com/doc/mysql/en/mysql-refresh.html)

### Значення, що повертаються

**`true`** у разі успішного виконання, **`false`** в іншому випадку.

### Дивіться також

-   [mysqli\_poll()](mysqli.poll.html) - Опитування підключень