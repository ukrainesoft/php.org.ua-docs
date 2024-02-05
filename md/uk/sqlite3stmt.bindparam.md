---
navigation:
  - class.sqlite3stmt.md: « SQLite3Stmt
  - sqlite3stmt.bindvalue.md: 'SQLite3Stmt::bindValue »'
  - index.md: PHP Manual
  - class.sqlite3stmt.md: SQLite3Stmt
title: 'SQLite3Stmt::bindParam'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3Stmt::bindParam

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::bindParam — Зв'язує параметр зі змінною підготовленого запиту

### Опис

```methodsynopsis
public SQLite3Stmt::bindParam(string|int $param, mixed &$var, int $type = SQLITE3_TEXT): bool
```

Зв'язує параметр із змінною підготовленого запиту.

**Застереження**

До PHP 7.2.14 та 7.3.0, [SQLite3Stmt::reset()](sqlite3stmt.reset.md) повинен викликатись до першого виклику [SQLite3Stmt::execute()](sqlite3stmt.execute.md)якщо потрібно, щоб пов'язане значення коректно оновлювалося при наступних викликах [SQLite3Stmt::execute()](sqlite3stmt.execute.md). Якщо метод [SQLite3Stmt::reset()](sqlite3stmt.reset.md) не викликався, то пов'язане значення не змінюватиметься, навіть якщо значення, надане змінною, переданою **SQLite3Stmt::bindParam()**, змінилося або знову було викликано метод **SQLite3Stmt::bindParam()**

### Список параметрів

`param`

Або рядок (string) (для іменованих параметрів), або ціле число (int) (для позитивних параметрів), що ідентифікує змінну підготовленого запиту, якого має бути прив'язане значення. Якщо іменований параметр не починається з двокрапки (( `:` )) або знаку `@`, автоматично додається двокрапка ( `:` ). Позитивні параметри починаються з першого.

`var`

Параметр для прив'язки до змінного підготовленого запиту.

`type`

Тип даних параметра для прив'язування.

-   **`SQLITE3_INTEGER`**: Значення є цілим числом зі знаком, яке зберігається в 1, 2, 3, 4, 6 або 8 байт, залежно від величини значення.
    
-   **`SQLITE3_FLOAT`**: Значення є числом з плаваючою точкою, яке зберігається у вигляді 8-байтного числа IEEE з плаваючою точкою.
    
-   **`SQLITE3_TEXT`**: Значення є текстовим рядком, який зберігається в кодуванні бази даних (UTF-8, UTF-16BE або UTF-16-LE).
    
-   **`SQLITE3_BLOB`**: Значення є великим двійковим об'єктом (blob) даних, який зберігається так само, як і вхідні дані.
    
-   **`SQLITE3_NULL`**: Значення є значенням NULL.
    

У PHP 7.0.7, якщо `type` опущений, то він автоматично визначається з типу `var`: bool та int розглядаються як **`SQLITE3_INTEGER`**, float як **`SQLITE3_FLOAT`**, null як **`SQLITE3_NULL`** і всі інші як **`SQLITE3_TEXT`**Раньше, если тип опущен, то по умолчанию использовался**`SQLITE3_TEXT`**

> **Зауваження** :
> 
> Якщо `var`равен\*\*`null`\*\*, він завжди обробляється як **`SQLITE3_NULL`**, независимо от заданного`type`

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо параметр прив'язаний до змінної підготовленого запиту, \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Параметр`param` тепер підтримує нотацію `@param` |

### Приклади

**Приклад #1 Приклад використання** SQLite3Stmt::bindParam()\*\*\*\*

У прикладі показано, як один підготовлений запит із прив'язкою одного параметра може використовуватися для вставки кількох рядків із різними значеннями.

```php
<?php
$db = new SQLite3(':memory:');
$db->exec("CREATE TABLE foo (bar TEXT)");

$stmt = $db->prepare("INSERT INTO foo VALUES (:bar)");
$stmt->bindParam(':bar', $bar, SQLITE3_TEXT);

$bar = 'baz';
$stmt->execute();

$bar = 42;
$stmt->execute();

$res = $db->query("SELECT * FROM foo");
while (($row = $res->fetchArray(SQLITE3_ASSOC))) {
    var_dump($row);
}
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["bar"]=>
  string(3) "baz"
}
array(1) {
  ["bar"]=>
  string(2) "42"
}
```

### Дивіться також

-   [SQLite3Stmt::bindValue()](sqlite3stmt.bindvalue.md) \- Зв'язує значення параметра зі змінною підготовленого запиту
-   [SQLite3::prepare()](sqlite3.prepare.md) \- готує SQL-запит для виконання
