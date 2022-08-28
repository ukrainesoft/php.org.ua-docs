Оновлення даних у таблиці

-   [« pg\_untrace](function.pg-untrace.html)
    
-   [pg\_version »](function.pg-version.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Оновлення даних у таблиці
    

# пгupdate

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгupdate — Оновлення даних у таблиці

### Опис

```methodsynopsis
pg_update(    PgSql\Connection $connection,    string $table_name,    array $values,    array $conditions,    int $flags = PGSQL_DML_EXEC): string|bool
```

**пгupdate()** замінює записи у таблиці, що задовольняють умовам `conditions` даними `values`

Якщо `flags` вказано, [pg\_convert()](function.pg-convert.html) застосовується до `values` із зазначеними прапорами.

За замовчуванням **пгupdate()** передає необроблені значення. Значення мають бути екрановані або опція **`PGSQL_DML_ESCAPE`** має бути вказана . **`PGSQL_DML_ESCAPE`** укладає в лапки та екранує параметри/ідентифікатори. Тому імена таблиць/стовпців стають чутливими до регістру.

Зверніть увагу, що ні екранування, ні підготовлений запит не захистять запит LIKE, JSON, масив, регулярні вирази і т.д. слід екранувати/перевіряти значення.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html)

`table_name`

Ім'я таблиці, де оновлюються записи.

`values`

Масив (array), ключі якого відповідають іменам колонок таблиці `table_name`, а значення замінять дані у цих колонках.

`condition`

Масив (array), ключі якого відповідають іменам колонок таблиці `table_name`. Буде оновлено лише рядки, значення полів яких збігатимуться зі значеннями масиву.

`flags`

Одна з констант **`PGSQL_CONV_OPTS`** **`PGSQL_DML_NO_CONV`** **`PGSQL_DML_ESCAPE`** **`PGSQL_DML_EXEC`** **`PGSQL_DML_ASYNC`** або **`PGSQL_DML_STRING`**або їх комбінація. Якщо `flags` містить **`PGSQL_DML_STRING`**, функція поверне рядок. Якщо встановлено **`PGSQL_DML_NO_CONV`** або **`PGSQL_DML_ESCAPE`**, то функція [pg\_convert()](function.pg-convert.html) внутрішньо не викликається.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Функція поверне рядок (string), якщо константа **`PGSQL_DML_STRING`** міститься в `flags`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгupdate()****

```php
<?php
  $db = pg_connect('dbname=foo');
  $data = array('field1'=>'AA', 'field2'=>'BB');

  // Это безопасно в некоторой степени, поскольку все значения экранируются.
  // Однако PostgreSQL поддерживает JSON/массив. Для этих значений это не безопасно
  // ни с через экранирование, ни с помощью подготовленного запроса.
  $res = pg_update($db, 'post_log', $_POST, $data);
  if ($res) {
      echo "Данные обновлены: $res\n";
  } else {
      echo "Должно быть переданы неверные данные\n";
  }
?>
```

### Дивіться також

-   [pg\_convert()](function.pg-convert.html) - Перетворює значення асоціативного масиву на прийнятні для використання в SQL-запитах