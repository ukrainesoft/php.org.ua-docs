---
navigation:
  - sqlite3.close.md: '« SQLite3::close'
  - sqlite3.createaggregate.md: 'SQLite3::createAggregate »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::\_\_construct — Створює екземпляр SQLite3 і відкриває з'єднання з базою

### Опис

public**SQLite3::\_\_construct**(string`$filename`, int`$flags`\= SQLITE3\_OPEN\_READWRITE | SQLITE3\_OPEN\_CREATE, string`$encryptionKey` = "")

Створює екземпляр SQLite3 і відкриває з'єднання з базою. Якщо увімкнено шифрування, з'являється можливість використання ключа.

### Список параметрів

`filename`

Путь к SQLite базе или`:memory:`для використання бази в оперативній пам'яті. Якщо `filename` встановити як порожній рядок, то буде створено приватну, тимчасову базу даних на диску. Ця база даних буде видалена одразу після закриття з'єднання з нею.

`flags`

Необов'язкові прапори для визначення типу відкриття бази даних. За замовчуванням використовується `SQLITE3_OPEN_READWRITE | SQLITE3_OPEN_CREATE`

-   `SQLITE3_OPEN_READONLY`: Відкрити тільки для читання
    
-   `SQLITE3_OPEN_READWRITE`: Відкрити для читання та запису.
    
-   `SQLITE3_OPEN_CREATE`: Створити новий файл бази даних, якщо він відсутній
    

`encryptionKey`

Необов'язковий ключ для шифрування/розшифрування бази даних. Якщо модуль шифрування не встановлено, цей параметр буде проігноровано.

### Помилки

Викидає виняток [Exception](class.exception.md)в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.0.10 | Параметр`filename` можна задавати порожнім рядком для створення на диску приватної бази даних. |

### Приклади

**Пример #1 Пример использования**SQLite3::\_\_construct()\*\*\*\*

```php
<?php
$db = new SQLite3('mysqlitedb.db');

$db->exec('CREATE TABLE foo (bar TEXT)');
$db->exec("INSERT INTO foo (bar) VALUES ('This is a test')");

$result = $db->query('SELECT bar FROM foo');
var_dump($result->fetchArray());
?>
```
