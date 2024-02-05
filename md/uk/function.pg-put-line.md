---
navigation:
  - function.pg-prepare.md: « pg\_prepare
  - function.pg-query-params.md: pg\_query\_params »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_put\_line
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_put\_line

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

pg\_put\_line — Передає на PostgreSQL сервер рядок із завершальним нулем

### Опис

```methodsynopsis
pg_put_line(PgSql\Connection $connection = ?, string $data): bool
```

**pg\_put\_line()** передає на PostgreSQL сервер рядок із завершальним нулем. Завершення рядка значенням NULL необхідно при його поєднанні з командою PostgreSQL `COPY FROM`

`COPY` є високошвидкісним інтерфейсом передачі, підтримуваним PostgreSQL. Дані передаються однією транзакцією та не розбираються парсером.

Як альтернативу можна використовувати функцію [pg\_copy\_from()](function.pg-copy-from.md)Она значительно проще в использовании.

> **Зауваження** :
> 
> Перед запуском функції [pg\_end\_copy()](function.pg-end-copy.md) програма повинна повідомити про сервер про завершення передачі даних, додавши в кінець останнього рядка символи "\\.".

**Увага**

Использование**pg\_put\_line()** може призвести до відмови операцій з великими об'єктами, що включають функції [pg\_lo\_read()](function.pg-lo-read.md) і [pg\_lo\_tell()](function.pg-lo-tell.md). Для цього використовуйте функції [pg\_copy\_from()](function.pg-copy-from.md) і [pg\_copy\_to()](function.pg-copy-to.md)

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Текстовий рядок для прямого пересилання на сервер. Завершальний `NULL` додається автоматично.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_put\_line()\*\*\*\*

```php
<?php
  $conn = pg_pconnect("dbname=foo");
  pg_query($conn, "create table bar (a int4, b char(16), d float8)");
  pg_query($conn, "copy bar from stdin");
  pg_put_line($conn, "3\thello world\t4.5\n");
  pg_put_line($conn, "4\tgoodbye world\t7.11\n");
  pg_put_line($conn, "\\.\n");
  pg_end_copy($conn);
?>
```

### Дивіться також

-   [pg\_end\_copy()](function.pg-end-copy.md) \- Синхронізує з бекендом PostgreSQL
