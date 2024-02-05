---
navigation:
  - function.pg-pconnect.md: « pg\_pconnect
  - function.pg-port.md: pg\_port »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_ping
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_ping

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_ping — Перевірити з'єднання з базою даних

### Опис

```methodsynopsis
pg_ping(?PgSql\Connection $connection = null): bool
```

**pg\_ping()** перевіряє з'єднання з базою даних та перепідключається, якщо воно порушено.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_ping()\*\*\*\*

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

if (!pg_ping($conn))
  die("Соединение нарушено\n");
?>
```

### Дивіться також

-   [pg\_connection\_status()](function.pg-connection-status.md) \- Визначає стан підключення
-   [pg\_connection\_reset()](function.pg-connection-reset.md) \- Скидання підключення (перепідключення)
