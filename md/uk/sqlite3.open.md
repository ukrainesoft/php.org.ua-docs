Відкрити базу даних SQLite

-   [« SQLite3::loadExtension](sqlite3.loadextension.md)
    
-   [SQLite3::openBlob »](sqlite3.openblob.md)
    
-   [PHP Manual](index.md)
    
-   [SQLite3](class.sqlite3.md)
    
-   Відкрити базу даних SQLite
    

# SQLite3::open

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::open — Відкрити базу даних SQLite

### Опис

```methodsynopsis
public SQLite3::open(string $filename, int $flags = SQLITE3_OPEN_READWRITE | SQLITE3_OPEN_CREATE, string $encryptionKey = ""): void
```

Відкриває базу даних SQLite 3. Якщо збірка включає шифрування, вона намагатиметься використовувати ключ.

### Список параметрів

`filename`

Шлях до БД SQLite або `:memory:` для використання БД у пам'яті.

`flags`

Опціональні прапори використовуються визначення, як відкривати БД. За замовчуванням `SQLITE3_OPEN_READWRITE | SQLITE3_OPEN_CREATE`

-   `SQLITE3_OPEN_READONLY`: Відкрити БД тільки для читання
    
-   `SQLITE3_OPEN_READWRITE`: Відкрити БД для читання та запису.
    
-   `SQLITE3_OPEN_CREATE`: Створити БД, якщо її немає
    

`encryptionKey`

Опціональний ключ для використання шифрування при роботі з БД. Якщо модуль шифрування не встановлений, ця опція не буде використана.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SQLite3::open()****

```php
<?php
/**
 * Простой пример расширения класса SQLite3 и изменения параметров конструктора.
 * После чего использование метода open для инициализации БД.
 */
class MyDB extends SQLite3
{
    function __construct()
    {
        $this->open('mysqlitedb.db');
    }
}

$db = new MyDB();

$db->exec('CREATE TABLE foo (bar STRING)');
$db->exec("INSERT INTO foo (bar) VALUES ('This is a test')");

$result = $db->query('SELECT bar FROM foo');
var_dump($result->fetchArray());
?>
```