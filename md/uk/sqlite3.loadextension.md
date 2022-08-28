Спробувати завантажити бібліотеку модуля SQLite

-   [« SQLite3::lastInsertRowID](sqlite3.lastinsertrowid.html)
    
-   [SQLite3::open »](sqlite3.open.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3](class.sqlite3.html)
    
-   Спробувати завантажити бібліотеку модуля SQLite
    

# SQLite3::loadExtension

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::loadExtension — Спробувати завантажити бібліотеку модуля SQLite

### Опис

```methodsynopsis
public SQLite3::loadExtension(string $name): bool
```

Спробувати завантажити бібліотеку модуля SQLite.

### Список параметрів

`name`

Ім'я бібліотеки, що завантажується. Бібліотека повинна знаходитись у каталозі, вказаному в конфігураційній опції sqlite3.extensiondir.

### Значення, що повертаються

Повертає **`true`** у випадку, якщо модуль успішно завантажено або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SQLite3::loadExtension()****

```php
<?php
$db = new SQLite3('mysqlitedb.db');
$db->loadExtension('libagg.so');
?>
```