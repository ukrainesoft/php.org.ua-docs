---
navigation:
  - function.pg-tty.md: « pg\_tty
  - function.pg-untrace.md: pg\_untrace »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_unescape\_bytea
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_unescape\_bytea

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_unescape\_bytea — Забирає екранування двійкових даних типу bytea

### Опис

```methodsynopsis
pg_unescape_bytea(string $string): string
```

**pg\_unescape\_bytea()** прибирає екранування спецсимволів у значеннях типу PostgreSQL bytea. Повертає неекранований рядок, що містить двійкові дані.

> **Зауваження** :
> 
> При вибірці SQL функцією `SELECT` даних типу bytea PostgreSQL повертає значення у восьмеричній системі числення з префіксом '\\' (такі як \\032). Користувачеві необхідно вручну перетворювати їх у двійковий формат.
> 
> Функція підтримується PostgreSQL версії 7.2 та вище. Для версій 7.2.0 та 7.2.1 значення мають бути перетворені до типу bytea, коли увімкнена мультибайтова підтримка. Тоді як `INSERT INTO test_table (image)VALUES ('$image_escaped'::bytea);` PostgreSQL 7.2.2 і вище не вимагає будь-яких перетворень. Виняток становить випадок, коли клієнтське (frontend) кодування не відповідає серверному (backend). При цьому виникає помилка мультибайтового потоку, і користувач повинен привести дані типу bytea, щоб її уникнути.

### Список параметрів

`string`

Рядок (string), що містить дані типу PostgreSQL bytea і підлягає перетворенню на двійковий рядок PHP.

### Значення, що повертаються

Рядок (string) з неекранованими спецсимволами.

### Приклади

**Приклад #1 Приклад використання** pg\_unescape\_bytea()\*\*\*\*

```php
<?php
  // Подключение к базе данных
  $dbconn = pg_connect('dbname=foo');

  // Получение bytea данных
  $res = pg_query("SELECT data FROM gallery WHERE name='Pine trees'");
  $raw = pg_fetch_result($res, 'data');

  // Преобразование в двоичный формат и отправка в броузер
  header('Content-type: image/jpeg');
  echo pg_unescape_bytea($raw);
?>
```

### Дивіться також

-   [pg\_escape\_bytea()](function.pg-escape-bytea.md) \- Екранує спецсимволи у рядку для вставки у поле типу bytea
-   [pg\_escape\_string()](function.pg-escape-string.md) \- Екранування спецсимволів у рядку запиту
