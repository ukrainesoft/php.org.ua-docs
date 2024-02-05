---
navigation:
  - pdo.pgsqlgetpid.md: '« PDO::pgsqlGetPid'
  - pdo.pgsqllobopen.md: 'PDO::pgsqlLOBOpen »'
  - index.md: PHP Manual
  - ref.pdo-pgsql.md: PostgreSQL (PDO)
title: 'PDO::pgsqlLOBCreate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::pgsqlLOBCreate

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL pdo\_pgsql >= 1.0.2)

PDO::pgsqlLOBCreate — Створити новий великий об'єкт (LOB)

### Опис

```methodsynopsis
public PDO::pgsqlLOBCreate(): string
```

Функция**PDO::pgsqlLOBCreate()** створює великий об'єкт (LOB) та повертає його OID. Ви можете відкрити потік для читання або зміни об'єкта за допомогою функції [PDO::pgsqlLOBOpen()](pdo.pgsqllobopen.md). OID можна зберегти в стовпці типу OID і використовувати як посилання на LOB, не викликаючи неконтрольованого збільшення розміру рядків. LOB буде жити в базі даних доки не буде видалено за допомогою функції [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.md)

Великі об'єкти можуть бути до 2ГБ розміром, але дуже громіздкі. Ви повинні переконатися, що виконали [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.md) до того, як видаліть останній рядок у вашій базі даних, яка посилається на його OID. До того ж великі об'єкти не мають контролю доступу. Як альтернативу спробуйте використовувати тип даних bytea. Останні версії PostgreSQL дозволяють стовпці типу bytea до 1ГБ розміром та прозоро керують табличним простором для оптимізації довжини рядків.

> **Зауваження**: Цю функцію необхідно виконувати у транзакції.

### Список параметрів

\*\*PDO::pgsqlLOBCreate()\*\*не принимает параметров.

### Значення, що повертаються

Повертає OID створеного об'єкта або **`false`**

### Приклади

**Пример #1 Пример использования**PDO::pgsqlLOBCreate()\*\*\*\*

У цьому прикладі створюється LOB і заповнюється даними з файлу. Після цього його OID зберігається у таблиці.

```php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$oid = $db->pgsqlLOBCreate();
$stream = $db->pgsqlLOBOpen($oid, 'w');
$local = fopen($filename, 'rb');
stream_copy_to_stream($local, $stream);
$local = null;
$stream = null;
$stmt = $db->prepare("INSERT INTO BLOBS (ident, oid) VALUES (?, ?)");
$stmt->execute(array($some_id, $oid));
$db->commit();
?>
```

### Дивіться також

-   [PDO::pgsqlLOBOpen()](pdo.pgsqllobopen.md) \- Відкриває потік для існуючого великого об'єкту
-   [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.md) \- Видалити великий об'єкт
-   [pg\_lo\_create()](function.pg-lo-create.md) \- Створює великий об'єкт
