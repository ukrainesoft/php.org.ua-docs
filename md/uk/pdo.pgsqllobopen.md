---
navigation:
  - pdo.pgsqllobcreate.md: '« PDO::pgsqlLOBCreate'
  - pdo.pgsqllobunlink.md: 'PDO::pgsqlLOBUnlink »'
  - index.md: PHP Manual
  - ref.pdo-pgsql.md: PostgreSQL (PDO)
title: 'PDO::pgsqlLOBOpen'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::pgsqlLOBOpen

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL pdo\_pgsql >= 1.0.2)

PDO::pgsqlLOBOpen — Відкриває потік для існуючого великого об'єкта

### Опис

```methodsynopsis
public PDO::pgsqlLOBOpen(string $oid, string $mode = "rb"): resource|false
```

Функция**PDO::pgsqlLOBOpen()** відкриває потік до великого об'єкта (LOB) заданого за допомогою `oid`. Якщо `mode`задан как`r`потік відкривається для читання. Якщо `mode`задан как`w`для запису. Для маніпуляції з потоком можна використовувати звичайні файлові функції, такі як [fread()](function.fread.md) [fwrite()](function.fwrite.md) і [fgets()](function.fgets.md)

> **Зауваження**: Ця функція та всі маніпуляції з LOB повинні відбуватися у транзакції.

### Список параметрів

`oid`

Ідентифікатор великого об'єкту.

`mode`

Якщо `r`то потік відкривається на читання. Якщо `w`то потік відкривається на запис.

### Значення, що повертаються

Повертає ресурс потоку у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**PDO::pgsqlLOBOpen()\*\*\*\*

Продолжая пример из описания[PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.md)Цей код витягує LOB з БД і виводить його в браузер.

```php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$stmt = $db->prepare("select oid from BLOBS where ident = ?");
$stmt->execute(array($some_id));
$stmt->bindColumn('oid', $oid, PDO::PARAM_STR);
$stmt->fetch(PDO::FETCH_BOUND);
$stream = $db->pgsqlLOBOpen($oid, 'r');
header("Content-type: application/octet-stream");
fpassthru($stream);
?>
```

### Дивіться також

-   [PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.md) \- Створити новий великий об'єкт (LOB)
-   [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.md) \- Видалити великий об'єкт
-   [pg\_lo\_open()](function.pg-lo-open.md) \- Відкриває великий об'єкт бази даних
