---
navigation:
  - sqlite3.setauthorizer.md: '« SQLite3::setAuthorizer'
  - class.sqlite3exception.md: SQLite3Exception »
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::version'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::version

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::version — Повертає версію бібліотеки SQLite3, містить як рядкову константу, так і цифрову

### Опис

```methodsynopsis
public static SQLite3::version(): array
```

Повертає версію бібліотеки SQLite3, містить як рядкову константу, так і цифрову.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив із ключами "versionString" та "versionNumber".

### Приклади

**Приклад #1 Приклад використання** SQLite3::version()\*\*\*\*

```php
<?php
print_r(SQLite3::version());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [versionString] => 3.5.9
    [versionNumber] => 3005009
)
```
