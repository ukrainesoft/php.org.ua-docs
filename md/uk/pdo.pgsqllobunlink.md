---
navigation:
  - pdo.pgsqllobopen.md: '« PDO::pgsqlLOBOpen'
  - ref.pdo-sqlite.html: SQLite (PDO) »
  - index.md: PHP Manual
  - ref.pdo-pgsql.html: PostgreSQL (PDO)
title: 'PDO::pgsqlLOBUnlink'
---
# PDO::pgsqlLOBUnlink

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL pdopgsql >= 1.0.2)

PDO::pgsqlLOBUnlink — Видалити великий об'єкт

### Опис

```methodsynopsis
public PDO::pgsqlLOBUnlink(string $oid): bool
```

Видаляє великий об'єкт (LOB) з БД з його OID.

> **Зауваження**: Цю функцію необхідно виконувати у транзакції.

### Список параметрів

`oid`

Ідентифікатор LOB

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **PDO::pgsqlLOBUnlink()****

У цьому прикладі ми видаляємо великий об'єкт з БД до того, як видалимо рядки з таблиці, що посилаються на нього, що зберігає інформацію про великі об'єкти, яку ми використовували в прикладах для функцій [PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.md) і [PDO::pgsqlLOBOpen()](pdo.pgsqllobopen.md)

```php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$db->pgsqlLOBUnlink($oid);
$stmt = $db->prepare("DELETE FROM BLOBS where ident = ?");
$stmt->execute(array($some_id));
$db->commit();
?>
```

### Дивіться також

-   [PDO::pgsqlLOBOpen()](pdo.pgsqllobopen.md) - Відкриває потік для існуючого великого об'єкту
-   [PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.md) - Створити новий великий об'єкт (LOB)
