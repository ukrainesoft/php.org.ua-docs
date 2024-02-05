---
navigation:
  - sqlite3stmt.bindparam.md: '« SQLite3Stmt::bindParam'
  - sqlite3stmt.clear.md: 'SQLite3Stmt::clear »'
  - index.md: PHP Manual
  - class.sqlite3stmt.md: SQLite3Stmt
title: 'SQLite3Stmt::bindValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3Stmt::bindValue

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::bindValue — Зв'язує значення параметра зі змінною підготовленого запиту

### Опис

```methodsynopsis
public SQLite3Stmt::bindValue(string|int $param, mixed $value, int $type = SQLITE3_TEXT): bool
```

Зв'язує значення параметра зі змінною підготовленого запиту.

**Застереження**

До PHP 7.2.14 та 7.3.0, якщо виконано запит, необхідно викликати метод [SQLite3Stmt::reset()](sqlite3stmt.reset.md) щоб можна було змінити значення пов'язаних параметрів.

### Список параметрів

`param`

Або рядок (string) (для іменованих параметрів), або ціле число (int) (для позитивних параметрів), що ідентифікує змінну підготовленого запиту, якого має бути прив'язане значення. Якщо іменований параметр не починається з двокрапки (( `:` )) або знаку `@`, автоматично додається двокрапка ( `:` ). Позитивні параметри починаються з першого.

`value`

Значення прив'язки до змінної підготовленого запиту.

`type`

Тип даних для прив'язки.

-   **`SQLITE3_INTEGER`**: Значення є цілим числом зі знаком, яке зберігається в 1, 2, 3, 4, 6 або 8 байт, залежно від величини значення.
    
-   **`SQLITE3_FLOAT`**: Значення є числом з плаваючою точкою, яке зберігається у вигляді 8-байтного числа IEEE з плаваючою точкою.
    
-   **`SQLITE3_TEXT`**: Значення є текстовим рядком, який зберігається в кодуванні бази даних (UTF-8, UTF-16BE або UTF-16-LE).
    
-   **`SQLITE3_BLOB`**: Значення є великим двійковим об'єктом (blob) даних, який зберігається так само, як і вхідні дані.
    
-   **`SQLITE3_NULL`**: Значення є значенням NULL.
    

У PHP 7.0.7, якщо `type` опущений, то він автоматично визначається з типу `param`: bool та int розглядаються як **`SQLITE3_INTEGER`**, float як **`SQLITE3_FLOAT`**, null як **`SQLITE3_NULL`** і всіх інших як **`SQLITE3_TEXT`**Раньше, если тип опущен, он по умолчанию использовался**`SQLITE3_TEXT`**

> **Зауваження** :
> 
> Якщо `param`равен\*\*`null`\*\*, він завжди обробляється як **`SQLITE3_NULL`**, независимо от заданного`type`

### Значення, що повертаються

Повертає **`true`**, якщо параметр прив'язаний до змінної підготовленого запиту або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Параметр`param` тепер підтримує нотацію `@param` |

### Приклади

**Приклад #1 Приклад використання** SQLite3Stmt::bindValue()\*\*\*\*

```php
<?php
$db = new SQLite3(':memory:');

$db->exec('CREATE TABLE foo (id INTEGER, bar STRING)');
$db->exec("INSERT INTO foo (id, bar) VALUES (1, 'This is a test')");

$stmt = $db->prepare('SELECT bar FROM foo WHERE id=:id');
$stmt->bindValue(':id', 1, SQLITE3_INTEGER);

$result = $stmt->execute();
var_dump($result->fetchArray(SQLITE3_ASSOC));
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["bar"]=>
  string(14) "This is a test"
}
```

### Дивіться також

-   [SQLite3Stmt::bindParam()](sqlite3stmt.bindparam.md) \- Зв'язує параметр із змінною підготовленого запиту
-   [SQLite3::prepare()](sqlite3.prepare.md) \- готує SQL-запит для виконання
