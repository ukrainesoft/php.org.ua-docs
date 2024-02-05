---
navigation:
  - function.pg-end-copy.md: « pg\_end\_copy
  - function.pg-escape-identifier.md: pg\_escape\_identifier »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_escape\_bytea
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_escape\_bytea

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_escape\_bytea - Екранує спецсимволи в рядку для вставки в поле типу bytea

### Опис

```methodsynopsis
pg_escape_bytea(PgSql\Connection $connection = ?, string $data): string
```

**pg\_escape\_bytea()** екранує спецсимволи у рядку з даними типу bytea. Повертає екранований рядок.

> **Зауваження** :
> 
> При вибірці SQL-функцією `SELECT` даних типу bytea PostgreSQL повертає значення у восьмеричній системі числення з префіксом '\\' (такі як \\032). Користувачеві необхідно вручну перетворювати їх у двійковий формат.
> 
> Функція підтримується PostgreSQL версії 7.2 та вище. Для версій 7.2.0 та 7.2.1 значення мають бути перетворені до типу bytea, коли увімкнена мультибайтова підтримка. Тоді як `INSERT INTO test_table (image)VALUES ('$image_escaped'::bytea);` PostgreSQL 7.2.2 і вище не вимагає будь-яких перетворень. Виняток становить випадок, коли клієнтське (frontend) кодування не відповідає серверному (backend). При цьому виникає помилка мультибайтового потоку, і користувач повинен привести дані типу bytea, щоб її уникнути.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Рядок містить двійкові дані у вигляді тексту, які потрібно помістити в поле типу bytea.

### Значення, що повертаються

Повертає рядок, де екрановані всі необхідні символи.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_escape\_bytea()\*\*\*\*

```php
<?php
  // Подключение к базе данных
  $dbconn = pg_connect('dbname=foo');

  // Чтение бинарного файла
  $data = file_get_contents('image1.jpg');

  // Экранирование спецсимволов в строке с двоичными данными
  $escaped = pg_escape_bytea($data);

  // Вставка в таблицу базы данных
  pg_query("INSERT INTO gallery (name, data) VALUES ('Pine trees', '{$escaped}')");
?>
```

### Дивіться також

-   [pg\_unescape\_bytea()](function.pg-unescape-bytea.md) \- Забирає екранування двійкових даних типу bytea
-   [pg\_escape\_string()](function.pg-escape-string.md) \- Екранування спецсимволів у рядку запиту
