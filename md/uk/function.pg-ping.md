---
navigation:
  - function.pg-pconnect.html: « pgpconnect
  - function.pg-port.html: пгport »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгping
---
# пгping

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгping — Перевірити з'єднання з базою даних

### Опис

```methodsynopsis
pg_ping(?PgSql\Connection $connection = null): bool
```

**пгping()** перевіряє з'єднання з базою даних та перепідключається, якщо воно порушено.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгping()****

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

if (!pg_ping($conn))
  die("Соединение нарушено\n");
?>
```

### Дивіться також

-   [пгconnectionstatus()](function.pg-connection-status.html) - Визначає стан підключення
-   [пгconnectionreset()](function.pg-connection-reset.html) - Скидання підключення (перепідключення)
