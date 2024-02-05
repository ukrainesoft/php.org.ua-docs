---
navigation:
  - function.pg-send-query.md: « pg\_send\_query
  - function.pg-set-error-context-visibility.md: pg\_set\_error\_context\_visibility »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_set\_client\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_set\_client\_encoding

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

pg\_set\_client\_encoding — Встановлює клієнтське кодування

### Опис

```methodsynopsis
pg_set_client_encoding(PgSql\Connection $connection = ?, string $encoding): int
```

**pg\_set\_client\_encoding()** встановлює клієнтське кодування та повертає 0 у разі успішного виконання, -1 у разі виникнення помилки.

PostgreSQL автоматично конвертує дані з кодування бази даних на кодування клієнтської програми.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_setclientencoding()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`encoding`

Необхідне клієнтське кодування. Список можливих значень: `SQL_ASCII` `EUC_JP` `EUC_CN` `EUC_KR` `EUC_TW` `UNICODE` `MULE_INTERNAL` `LATINX`(X=1...9),`KOI8` `WIN` `ALT` `SJIS` `BIG5`or`WIN1250`

Список доступних кодувань залежить від версії PostgreSQL. Дивіться документацію до вашої версії сервера.

### Значення, що повертаються

Повертає у разі успішного виконання, або `-1`в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_set\_client\_encoding()\*\*\*\*

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

// Установка кодировки в UNICODE. Данные будут автоматически
// преобразованы из кодировки в базе данных к клиентской.
pg_set_client_encoding($conn, "UNICODE");

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

// Выводим UTF-8 данные
while ($row = pg_fetch_row($result)) {
  echo "Author: $row[0]  E-mail: $row[1]";
  echo "<br />\n";
}

?>
```

### Дивіться також

-   [pg\_client\_encoding()](function.pg-client-encoding.md) \- отримання кодування клієнта.
