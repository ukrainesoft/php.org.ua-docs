Встановлює клієнтське кодування

-   [« pg\_send\_query](function.pg-send-query.html)
    
-   [pg\_set\_error\_verbosity »](function.pg-set-error-verbosity.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Встановлює клієнтське кодування
    

# пгsetclientencoding

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

пгsetclientencoding — Встановлює клієнтське кодування

### Опис

```methodsynopsis
pg_set_client_encoding(PgSql\Connection $connection = ?, string $encoding): int
```

**пгsetclientencoding()** встановлює клієнтське кодування та повертає 0 у разі успішного виконання, -1 у разі виникнення помилки.

PostgreSQL автоматично конвертує дані з кодування бази даних на кодування клієнтської програми.

> **Зауваження**
> 
> Колишня назва функції: **пгsetclientencoding()**

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`encoding`

Необхідне клієнтське кодування. Список можливих значень: `SQL_ASCII` `EUC_JP` `EUC_CN` `EUC_KR` `EUC_TW` `UNICODE` `MULE_INTERNAL` `LATINX` (X = 1 ... 9), `KOI8` `WIN` `ALT` `SJIS` `BIG5` ор `WIN1250`

Список доступних кодувань залежить від версії PostgreSQL. Дивіться документацію до вашої версії сервера.

### Значення, що повертаються

Повертає `0` у разі успішного виконання, або `-1` у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгsetclientencoding()****

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

// Установка кодировки в UNICODE. Данные будут автоматически
// преобразованы из кодировки в базе данных к клиентской.
pg_set_client_encoding($conn, "UNICODE");

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

// Выводим UTF-8 данные
while ($row = pg_fetch_row($result)) {
  echo "Author: $row[0]  E-mail: $row[1]";
  echo "<br />\n";
}

?>
```

### Дивіться також

-   [pg\_client\_encoding()](function.pg-client-encoding.html) - отримання кодування клієнта.