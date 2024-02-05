---
navigation:
  - function.pg-free-result.md: « pg\_free\_result
  - function.pg-get-pid.md: pg\_get\_pid »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_get\_notify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_get\_notify

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_get\_notify — Отримання SQL NOTIFY повідомлення

### Опис

```methodsynopsis
pg_get_notify(PgSql\Connection $connection, int $mode = PGSQL_ASSOC): array|false
```

**pg\_get\_notify()** отримує повідомлення, згенеровані командою SQL `NOTIFY`Для получения уведомлений используйте команду SQL`LISTEN`

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`**и**`PGSQL_BOTH`**При использовании**`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Масив (array), що містить повідомлення `NOTIFY` та PID сервера БД. Якщо підтримується сервером, масив також містить версію сервера та корисне навантаження. Якщо жодних повідомлень не очікується, функція поверне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Повідомлення PostgreSQL NOTIFY**

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

// Слушаем сообщение 'author_updated' из другого процесса
pg_query($conn, 'LISTEN author_updated;');
$notify = pg_get_notify($conn);
if (!$notify) {
  echo "Нет сообщений\n";
} else {
  print_r($notify);
}
?>
```

### Дивіться також

-   [pg\_get\_pid()](function.pg-get-pid.md) \- Отримує ID процесу сервера БД
