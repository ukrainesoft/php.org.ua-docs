---
navigation:
  - mysqli.reap-async-query.md: '« mysqli::reapasyncquery'
  - mysqli.release-savepoint.md: 'mysqli::releasesavepoint »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::refresh'
---
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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

`flags`

Налаштування оновлення задаються константами MYSQLIREFRESH, які описані у розділі документації [Константи MySQLi](mysqli.constants.md)

Дивіться також офіційну документацію [» MySQL Refresh](http://dev.mysql.com/doc/mysql/en/mysql-refresh.md)

### Значення, що повертаються

**`true`** у разі успішного виконання, **`false`** в іншому випадку.

### Дивіться також

-   [mysqlipoll()](mysqli.poll.md) - Опитування підключень
