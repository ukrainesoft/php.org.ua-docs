Скинути дані вихідного запиту на з'єднанні

-   [« pgfieldtype](function.pg-field-type.html)
    
-   [пгfreeresult »](function.pg-free-result.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Скинути дані вихідного запиту на з'єднанні
    

# пгflush

(PHP 5> = 5.6.0, PHP 7, PHP 8)

пгflush — Скинути дані вихідного запиту на з'єднанні

### Опис

```methodsynopsis
pg_flush(PgSql\Connection $connection): int|bool
```

**пгflush()** скидає будь-які дані вихідного запиту, що очікують надсилання на з'єднанні.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

### Значення, що повертаються

Повертає **`true`**, якщо скидання було успішним або дані не очікували скидання, або `0`, якщо частина очікуваних даних була скинута, однак залишилися ще **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |