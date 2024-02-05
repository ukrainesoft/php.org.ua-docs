---
navigation:
  - mysqli.reap-async-query.md: '« mysqli::reap\_async\_query'
  - mysqli.release-savepoint.md: 'mysqli::release\_savepoint »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::refresh'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::refresh

# mysqli\_refresh

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

mysqli::refresh -- mysqli\_refresh — Оновлення

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`flags`

Налаштування оновлення задаються константами MYSQLI\_REFRESH\_\*, які описані у розділі документації [Константи MySQLi](mysqli.constants.md)

Смотрите также официальную документацию[» MySQL Refresh](http://dev.mysql.com/doc/mysql/en/mysql-refresh.md)

### Значення, що повертаються

**`true`** у разі успішного виконання, **`false`** в іншому випадку.

### Дивіться також

-   [mysqli\_poll()](mysqli.poll.md) \- Опитування підключень
