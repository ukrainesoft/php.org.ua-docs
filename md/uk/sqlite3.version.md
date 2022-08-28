Повертає версію бібліотеки SQLite3, містить як рядкову константу, так і цифрову

-   [« SQLite3::setAuthorizer](sqlite3.setauthorizer.html)
    
-   [SQLite3Stmt »](class.sqlite3stmt.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite3](class.sqlite3.html)
    
-   Повертає версію бібліотеки SQLite3, містить як рядкову константу, так і цифрову
    

# SQLite3::version

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SQLite3::version — Повертає версію бібліотеки SQLite3, містить як рядкову константу, так і цифрову

### Опис

```methodsynopsis
public static SQLite3::version(): array
```

Повертає версію бібліотеки SQLite3, містить рядкову константу, так і числову.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив із ключами "versionString" та "versionNumber".

### Приклади

**Приклад #1 Приклад використання **SQLite3::version()****

```php
<?php
print_r(SQLite3::version());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [versionString] => 3.5.9
    [versionNumber] => 3005009
)
```