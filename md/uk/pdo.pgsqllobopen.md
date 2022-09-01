---
navigation:
  - pdo.pgsqllobcreate.html: '« PDO::pgsqlLOBCreate'
  - pdo.pgsqllobunlink.html: 'PDO::pgsqlLOBUnlink »'
  - index.html: PHP Manual
  - ref.pdo-pgsql.html: PostgreSQL (PDO)
title: 'PDO::pgsqlLOBOpen'
---
# PDO::pgsqlLOBOpen

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL pdopgsql >= 1.0.2)

PDO::pgsqlLOBOpen — Відкриває потік для існуючого великого об'єкта

### Опис

```methodsynopsis
public PDO::pgsqlLOBOpen(string $oid, string $mode = "rb"): resource|false
```

Функція **PDO::pgsqlLOBOpen()** відкриває потік до великого об'єкта (LOB) заданого за допомогою `oid`. Якщо `mode` заданий як `r`потік відкривається для читання. Якщо `mode` заданий як `w`для запису. Для маніпуляції з потоком можна використовувати звичайні файлові функції, такі як [fread()](function.fread.html) [fwrite()](function.fwrite.html) і [fgets()](function.fgets.html)

> **Зауваження**: Ця функція та всі маніпуляції з LOB повинні відбуватися у транзакції.

### Список параметрів

`oid`

Ідентифікатор великого об'єкту.

`mode`

Якщо `r`то потік відкривається на читання. Якщо `w`то потік відкривається на запис.

### Значення, що повертаються

Повертає ресурс потоку у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **PDO::pgsqlLOBOpen()****

Продовжуючи приклад з опису [PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.html)Цей код витягує LOB з БД і виводить його в браузер.

```php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$stmt = $db->prepare("select oid from BLOBS where ident = ?");
$stmt->execute(array($some_id));
$stmt->bindColumn('oid', $oid, PDO::PARAM_STR);
$stmt->fetch(PDO::FETCH_BOUND);
$stream = $db->pgsqlLOBOpen($oid, 'r');
header("Content-type: application/octet-stream");
fpassthru($stream);
?>
```

### Дивіться також

-   [PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.html) - Створити новий великий об'єкт (LOB)
-   [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.html) - Видалити великий об'єкт
-   [пглоopen()](function.pg-lo-open.html) - Відкриває великий об'єкт бази даних
