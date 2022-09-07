---
navigation:
  - function.pg-end-copy.md: « pgendcopy
  - function.pg-escape-identifier.md: пгescapeidentifier »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгescapebytea
---
# пгescapebytea

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгescapebytea - Екранує спецсимволи в рядку для вставки в поле типу bytea

### Опис

```methodsynopsis
pg_escape_bytea(PgSql\Connection $connection = ?, string $data): string
```

**пгescapebytea()** екранує спецсимволи у рядку з даними типу bytea. Повертає екранований рядок.

> **Зауваження**
> 
> При вибірці SQL-функцією `SELECT` даних типу bytea PostgreSQL повертає значення у восьмеричній системі числення з префіксом '' (такі як 032). Користувачеві необхідно вручну перетворювати їх на двійковий формат.
> 
> Функція підтримується PostgreSQL версії 7.2 та вище. Для версій 7.2.0 та 7.2.1 значення мають бути перетворені до типу bytea, коли увімкнена мультибайтова підтримка. Тоді як `INSERT INTO test_table (image)VALUES ('$image_escaped'::bytea);` PostgreSQL 7.2.2 і вище не вимагає будь-яких перетворень. Виняток становить випадок, коли клієнтське (frontend) кодування не відповідає серверному (backend). При цьому виникає помилка мультибайтового потоку, і користувач повинен привести дані типу bytea, щоб її уникнути.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`data`

Рядок містить двійкові дані у вигляді тексту, які потрібно помістити в поле типу bytea.

### Значення, що повертаються

Повертає рядок, де екрановані всі необхідні символи.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгescapebytea()****

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

-   [пгunescapebytea()](function.pg-unescape-bytea.md) - Забирає екранування двійкових даних типу bytea
-   [пгescapestring()](function.pg-escape-string.md) - Екранування спецсимволів у рядку запиту
