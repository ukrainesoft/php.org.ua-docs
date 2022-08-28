Створити новий великий об'єкт (LOB)

-   [« PDO::pgsqlGetPid](pdo.pgsqlgetpid.html)
    
-   [PDO::pgsqlLOBOpen »](pdo.pgsqllobopen.html)
    
-   [PHP Manual](index.html)
    
-   [PostgreSQL (PDO)](ref.pdo-pgsql.html)
    
-   Створити новий великий об'єкт (LOB)
    

# PDO::pgsqlLOBCreate

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL pdopgsql >= 1.0.2)

PDO::pgsqlLOBCreate — Створити новий великий об'єкт (LOB)

### Опис

```methodsynopsis
public PDO::pgsqlLOBCreate(): string
```

Функція **PDO::pgsqlLOBCreate()** створює великий об'єкт (LOB) та повертає його OID. Ви можете відкрити потік для читання або зміни об'єкта за допомогою функції [PDO::pgsqlLOBOpen()](pdo.pgsqllobopen.html). OID можна зберегти в стовпці типу OID і використовувати як посилання на LOB, не викликаючи неконтрольованого збільшення розміру рядків. LOB буде жити в базі даних доки не буде видалено за допомогою функції [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.html)

Великі об'єкти можуть бути до 2ГБ розміром, але дуже громіздкі. Ви повинні переконатися, що виконали [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.html) до того, як видаліть останній рядок у вашій базі даних, яка посилається на його OID. До того ж великі об'єкти не мають контролю доступу. Як альтернативу спробуйте використовувати тип даних bytea. Останні версії PostgreSQL дозволяють стовпці типу bytea до 1ГБ розміром та прозоро керують табличним простором для оптимізації довжини рядків.

> **Зауваження**: Цю функцію необхідно виконувати у транзакції.

### Список параметрів

**PDO::pgsqlLOBCreate()** не приймає параметрів.

### Значення, що повертаються

Повертає OID створеного об'єкта або **`false`**

### Приклади

**Приклад #1 Приклад використання **PDO::pgsqlLOBCreate()****

У цьому прикладі створюється LOB і заповнюється даними з файлу. Після цього його OID зберігається у таблиці.

```php
<?php
$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);
$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
$db->beginTransaction();
$oid = $db->pgsqlLOBCreate();
$stream = $db->pgsqlLOBOpen($oid, 'w');
$local = fopen($filename, 'rb');
stream_copy_to_stream($local, $stream);
$local = null;
$stream = null;
$stmt = $db->prepare("INSERT INTO BLOBS (ident, oid) VALUES (?, ?)");
$stmt->execute(array($some_id, $oid));
$db->commit();
?>
```

### Дивіться також

-   [PDO::pgsqlLOBOpen()](pdo.pgsqllobopen.html) - Відкриває потік для існуючого великого об'єкту
-   [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.html) - Видалити великий об'єкт
-   [pg\_lo\_create()](function.pg-lo-create.html) - Створює великий об'єкт