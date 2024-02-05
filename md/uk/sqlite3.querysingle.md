---
navigation:
  - sqlite3.query.md: '« SQLite3::query'
  - sqlite3.setauthorizer.md: 'SQLite3::setAuthorizer »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::querySingle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::querySingle

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::querySingle — Виконує запит і повертає одиночний результат

### Опис

```methodsynopsis
public SQLite3::querySingle(string $query, bool $entireRow = false): mixed
```

Виконує запит та повертає одиночний результат.

### Список параметрів

`query`

SQL запит на виконання.

`entireRow`

По умолчанию, функция**querySingle()** повертає значення першого стовпця, який повертається запитом. Якщо параметр `entireRow`является\*\*`true`\*\*, То запит повертає масив всього першого ряду.

### Значення, що повертаються

Повертає значення першого стовпця результатів або масив першого рядка (якщо параметр `entireRow`является\*\*`true`\*\*

Якщо запит коректний, але результат порожній, то повернеться **`null`**, якщо параметр `entireRow`является\*\*`false`\*\*, інакше повертається порожній масив.

Неправильний або відсутній запит повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** SQLite3::querySingle()\*\*\*\*

```php
<?php
$db = new SQLite3('mysqlitedb.db');

var_dump($db->querySingle('SELECT username FROM user WHERE userid=1'));
print_r($db->querySingle('SELECT username, email FROM user WHERE userid=1', true));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "Scott"
Array
(
    [username] => Scott
    [email] => scott@example.com
)
```
