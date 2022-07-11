- [« PDO::pgsqlLOBCreate](pdo.pgsqllobcreate.md)
- [PDO::pgsqlLOBUnlink »](pdo.pgsqllobunlink.md)

- [PHP Manual](index.md)
- [PostgreSQL (PDO)](ref.pdo-pgsql.md)
- Відкриває потік для існуючого великого об'єкту

# PDO::pgsqlLOBOpen

(PHP 5 = 5.1.2, PHP 7, PHP 8, PECL pdo_pgsql = 1.0.2)

PDO::pgsqlLOBOpen — Відкриває потік для наявного великого об'єкта

### Опис

public **PDO::pgsqlLOBOpen**(string `$oid`, string `$mode` = "rb"):
resource\|false

Функція **PDO::pgsqlLOBOpen()** відкриває потік до великого об'єкта (LOB)
заданому за допомогою `oid`. Якщо `mode` заданий як `r`, потік відкривається
для читання. Якщо `mode` заданий як `w`, то для запису. Для маніпуляції з
потоком можна використовувати звичайні файлові функції, такі як
[fread()](function.fread.md), [fwrite()](function.fwrite.md) та
[fgets()](function.fgets.md).

> **Примітка**: Ця функція та всі маніпуляції з LOB повинні здійснюватися
> у транзакції.

### Список параметрів

`oid`
Ідентифікатор великого об'єкту.

`mode`
Якщо `r`, то потік відкривається читання. Якщо `w`, то потік відкривається
на запис.

### Значення, що повертаються

Повертає ресурс потоку у разі успішного виконання або **`false`**
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **PDO::pgsqlLOBOpen()****

Продовжуючи приклад з опису
[PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.md), цей код витягує LOB
з БД та виводить його в браузер.

` <?php$db = new PDO('pgsql:dbname=test host=localhost', $user, $pass);$db->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);$db->beginTransaction ();$stmt==$db->prepare("select oid from BLOBS whereident==??");$stmt->execute(array($some_id));$stmt->bindColumn('oid', $oid, PDO::PARAM_STR);$stmt->fetch(PDO::FETCH_BOUND);$stream = $db->pgsqlLOBOpen($oid, 'r');header("Content-type: application/octet-stream"); fpassthru($stream);?> `

### Дивіться також

- [PDO::pgsqlLOBCreate()](pdo.pgsqllobcreate.md) - Створити новий
великий об'єкт (LOB)
- [PDO::pgsqlLOBUnlink()](pdo.pgsqllobunlink.md) - Видалити великий
об'єкт
- [pg_lo_open()](function.pg-lo-open.md) - Відкриває великий об'єкт
бази даних
