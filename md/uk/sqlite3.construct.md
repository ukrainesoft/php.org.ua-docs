Створює екземпляр SQLite3 і відкриває з'єднання з базою

-   [« SQLite3::close](sqlite3.close.html)
    
-   [SQLite3::createAggregate »](sqlite3.createaggregate.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3](class.sqlite3.html)
    
-   Створює екземпляр SQLite3 і відкриває з'єднання з базою
    

# SQLite3::construct

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::construct — Створює екземпляр SQLite3 і відкриває з'єднання з базою

### Опис

public **SQLite3::construct**(string `$filename`, int `$flags` = SQLITE3OPENREADWRITE | SQLITE3OPENCREATE, string `$encryptionKey` = "")

Створює екземпляр SQLite3 і відкриває з'єднання з базою. Якщо увімкнено шифрування, з'являється можливість використання ключа.

### Список параметрів

`filename`

Шлях до SQLite бази або `:memory:`для використання бази в оперативній пам'яті. Якщо `filename` встановити як порожній рядок, то буде створено приватну, тимчасову базу даних на диску. Ця база даних буде видалена одразу після закриття з'єднання з нею.

`flags`

Необов'язкові прапори для визначення типу відкриття бази даних. За замовчуванням використовується `SQLITE3_OPEN_READWRITE | SQLITE3_OPEN_CREATE`

-   `SQLITE3_OPEN_READONLY`: Відкрити тільки для читання
    
-   `SQLITE3_OPEN_READWRITE`: Відкрити для читання та запису.
    
-   `SQLITE3_OPEN_CREATE`: Створити новий файл бази даних, якщо він відсутній
    

`encryptionKey`

Необов'язковий ключ для шифрування/розшифрування бази даних. Якщо модуль шифрування не встановлено, цей параметр буде проігноровано.

### Помилки

Викидає виняток [Exception](class.exception.html) у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `filename` можна задавати порожнім рядком для створення на диску приватної бази даних. |

### Приклади

**Приклад #1 Приклад використання **SQLite3::construct()****

```php
<?php
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE foo (bar TEXT)');
$db->exec("INSERT INTO foo (bar) VALUES ('This is a test')");

$result = $db->query('SELECT bar FROM foo');
var_dump($result->fetchArray());
?>
```