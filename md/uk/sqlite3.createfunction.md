---
navigation:
  - sqlite3.createcollation.md: '« SQLite3::createCollation'
  - sqlite3.enableexceptions.md: 'SQLite3::enableExceptions »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::createFunction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::createFunction

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::createFunction — Реєструє функцію PHP для використання як скалярну функцію SQL

### Опис

```methodsynopsis
public SQLite3::createFunction(    string $name,    callable $callback,    int $argCount = -1,    int $flags = 0): bool
```

Реєструє функцію PHP або функцію користувача для використання в якості скалярної функції SQL для використання в SQL-виразах.

### Список параметрів

`name`

Ім'я створюваної або перевизначуваної функції SQL.

`callback`

Ім'я функції PHP або функції користувача, що використовується як callback, що визначає поведінку функції SQL.

Функція має бути визначена як:

```methodsynopsis
callback(mixed $value, mixed ...$values): mixed
```

`value`

Перший аргумент, який передається функції SQL.

`values`

Додаткові аргументи, які передаються функції SQL.

`argCount`

Число аргументів, що приймаються функцією SQL. Якщо цей параметр дорівнює `-1`, то функція SQL може приймати будь-яку кількість аргументів.

`flags`

Побітове поєднання прапорів. В даний час підтримується тільки **`SQLITE3_DETERMINISTIC`**, який вказує, що функція завжди повертає той самий результат, враховуючи одні й самі вхідні дані всередині одного SQL-выражения.

### Значення, що повертаються

Повертає **`true`** у разі успішного створення функції або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.4 | Добавлен параметр`flags` |

### Приклади

**Пример #1 Пример использования**SQLite3::createFunction()\*\*\*\*

```php
<?php
function my_udf_md5($string) {
    return md5($string);
}

$db = new SQLite3('mysqlitedb.db');
$db->createFunction('my_udf_md5', 'my_udf_md5');

var_dump($db->querySingle('SELECT my_udf_md5("test")'));
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(32) "098f6bcd4621d373cade4e832627b4f6"
```
