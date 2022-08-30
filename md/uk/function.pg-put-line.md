Передає на PostgreSQL сервер рядок із завершальним нулем

-   [« pgprepare](function.pg-prepare.html)
    
-   [пгqueryparams »](function.pg-query-params.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
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

Як альтернативу можна використовувати функцію [пгcopyfrom()](function.pg-copy-from.html). Вона значно простіша у використанні.

> **Зауваження**
> 
> Перед запуском функції [пгendcopy()](function.pg-end-copy.html) програма повинна повідомити про сервер про завершення передачі даних, додавши в кінець останнього рядка символи ".".

**Увага**

Використання **пгputline()** може призвести до відмови операцій з великими об'єктами, що включають функції [пглоread()](function.pg-lo-read.html) і [пглоtell()](function.pg-lo-tell.html). Для цього використовуйте функції [пгcopyfrom()](function.pg-copy-from.html) і [пгcopyto()](function.pg-copy-to.html)

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.html) або [пгpconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Текстовий рядок для прямого пересилання на сервер. Завершальний `NULL` додається автоматично.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

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

-   [пгendcopy()](function.pg-end-copy.html) - Синхронізує з бекендом PostgreSQL