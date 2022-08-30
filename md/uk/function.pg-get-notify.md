Отримання SQL NOTIFY повідомлення

-   [« pgfreeresult](function.pg-free-result.html)
    
-   [пгgetpid »](function.pg-get-pid.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Отримання SQL NOTIFY повідомлення
    

# пгgetnotify

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгgetnotify — Отримання SQL NOTIFY повідомлення

### Опис

```methodsynopsis
pg_get_notify(PgSql\Connection $connection, int $mode = PGSQL_ASSOC): array|false
```

**пгgetnotify()** отримує повідомлення, згенеровані командою SQL `NOTIFY`. Для отримання повідомлень скористайтеся командою SQL `LISTEN`

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`** і **`PGSQL_BOTH`**. При використанні **`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Масив (array), що містить повідомлення `NOTIFY` та PID сервера БД. Якщо підтримується сервером, масив також містить версію сервера та корисне навантаження. Якщо жодних повідомлень не очікується, функція поверне **`false`**

### список змін

| Версия | Описание                                                                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Повідомлення PostgreSQL NOTIFY**

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

// Слушаем сообщение 'author_updated' из другого процесса
pg_query($conn, 'LISTEN author_updated;');
$notify = pg_get_notify($conn);
if (!$notify) {
  echo "Нет сообщений\n";
} else {
  print_r($notify);
}
?>
```

### Дивіться також

-   [пгgetpid()](function.pg-get-pid.html) - Отримує ID процесу сервера БД