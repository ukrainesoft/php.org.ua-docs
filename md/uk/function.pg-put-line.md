Передає на PostgreSQL сервер рядок із завершальним нулем

-   [« pg\_prepare](function.pg-prepare.html)
    
-   [pg\_query\_params »](function.pg-query-params.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Передає на PostgreSQL сервер рядок із завершальним нулем
    

# пгputline

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

пгputline — Передає на PostgreSQL сервер рядок із завершальним нулем

### Опис

```methodsynopsis
pg_put_line(PgSql\Connection $connection = ?, string $data): bool
```

**пгputline()** передає на PostgreSQL сервер рядок із завершальним нулем. Завершення рядка значенням NULL необхідно при його поєднанні з командою PostgreSQL `COPY FROM`

`COPY` є високошвидкісним інтерфейсом передачі, підтримуваним PostgreSQL. Дані передаються однією транзакцією та не розбираються парсером.

Як альтернативу можна використовувати функцію [pg\_copy\_from()](function.pg-copy-from.html). Вона значно простіша у використанні.

> **Зауваження**
> 
> Перед запуском функції [pg\_end\_copy()](function.pg-end-copy.html) програма повинна повідомити про сервер про завершення передачі даних, додавши в кінець останнього рядка символи ".".

**Увага**

Використання **пгputline()** може призвести до відмови операцій з великими об'єктами, що включають функції [pg\_lo\_read()](function.pg-lo-read.html) і [pg\_lo\_tell()](function.pg-lo-tell.html). Для цього використовуйте функції [pg\_copy\_from()](function.pg-copy-from.html) і [pg\_copy\_to()](function.pg-copy-to.html)

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Текстовий рядок для прямого пересилання на сервер. Завершальний `NULL` додається автоматично.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгputline()****

```php
<?php
  $conn = pg_pconnect("dbname=foo");
  pg_query($conn, "create table bar (a int4, b char(16), d float8)");
  pg_query($conn, "copy bar from stdin");
  pg_put_line($conn, "3\thello world\t4.5\n");
  pg_put_line($conn, "4\tgoodbye world\t7.11\n");
  pg_put_line($conn, "\\.\n");
  pg_end_copy($conn);
?>
```

### Дивіться також

-   [pg\_end\_copy()](function.pg-end-copy.html) - Синхронізує з бекендом PostgreSQL