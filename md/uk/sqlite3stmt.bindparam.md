- [«SQLite3Stmt](class.sqlite3stmt.md)
- [SQLite3Stmt::bindValue »](sqlite3stmt.bindvalue.md)

- [PHP Manual](index.md)
- [SQLite3Stmt](class.sqlite3stmt.md)
- Зв'язує параметр зі змінною підготовленого запиту

# SQLite3Stmt::bindParam

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

SQLite3Stmt::bindParam — Зв'язує параметр зі змінною підготовленого
запиту

### Опис

public **SQLite3Stmt::bindParam**(string\|int `$param`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`&$var`, int `$type` = **`SQLITE3_TEXT`**): bool

Зв'язує параметр із змінною підготовленого запиту.

**Застереження**

До PHP 7.2.14 та 7.3.0, [SQLite3Stmt::reset()](sqlite3stmt.reset.md)
повинен викликатись до першого виклику
[SQLite3Stmt::execute()](sqlite3stmt.execute.md), якщо треба, щоб
пов'язане значення коректно оновлювалося за наступних викликів
[SQLite3Stmt::execute()](sqlite3stmt.execute.md). Якщо метод
[SQLite3Stmt::reset()](sqlite3stmt.reset.md) не викликався, то
пов'язане значення не змінюватиметься, навіть якщо значення, надане
змінної, переданої **SQLite3Stmt::bindParam()**, змінилося або
знову був викликаний метод SQLite3Stmt::bindParam()**.

### Список параметрів

`param`
Або рядок (string) (для іменованих параметрів), або ціле число
(int) (для позитивних параметрів), що ідентифікує змінну
підготовленого запиту, якого має бути прив'язане значення. Якщо
іменований параметр не починається з двокрапки ((`:`)) або знака `@`,
автоматично додається двокрапка (`:`). Позитивні параметри
починаються з першого.

`var`
Параметр для прив'язки до змінного підготовленого запиту.

`type`
Тип параметру для прив'язки.

- **`SQLITE3_INTEGER`**: Значення є цілим числом зі знаком,
яке зберігається в 1, 2, 3, 4, 6 або 8 байт залежно від
величини значення.

- **`SQLITE3_FLOAT`**: Значення є числом з плаваючою точкою,
яке зберігається у вигляді 8-байтного числа IEEE з плаваючою точкою.

- **`SQLITE3_TEXT`**: Значення є текстовим рядком, яке
зберігається у кодуванні бази даних (UTF-8, UTF-16BE або UTF-16-LE).

- **`SQLITE3_BLOB`**: Значення є великим двійковим об'єктом
(blob) даних, який зберігається так само, як і вхідні дані.

- **`SQLITE3_NULL`**: Значення є NULL-значенням.

У PHP 7.0.7, якщо `type` опущений, він автоматично визначається з
типу `var`: bool та int розглядаються як **`SQLITE3_INTEGER`**, float
як **`SQLITE3_FLOAT`**, null як **`SQLITE3_NULL`** і всі інші як
**`SQLITE3_TEXT`**. Раніше якщо тип опущений, то за замовчуванням
використовувався **`SQLITE3_TEXT`**.

> **Примітка**:
>
> Якщо `var` дорівнює **`null`**, він завжди обробляється як
> **`SQLITE3_NULL`**, незалежно від заданого `type`.

### Значення, що повертаються

Повертає **`true`**, якщо параметр прив'язаний до змінної
підготовленого запиту, **`false`** у разі виникнення помилки.

### Список змін

| Версія | Опис                                           |
|--------|------------------------------------------------|
| 7.4.0  | Параметр param тепер підтримує нотацію @param. |

### Приклади

**Приклад #1 Приклад використання **SQLite3Stmt::bindParam()****

У прикладі показано, як один підготовлений запит із прив'язкою одного
параметра може використовуватися для вставки декількох рядків з різними
значеннями.

` <?php$db = new SQLite3(':memory:');$db->exec("CREATE TABLE foo (bar TEXT)");$stmt = $db->prepare("INSERT INTO foo VALUES (: bar)");$stmt->bindParam(':bar', $bar, SQLITE3_TEXT);$bar = 'baz';$stmt->execute();$bar = 42;$stmt->execute(); $res = $db->query("SELECT * FROM foo");while (($row = $res->fetchArray(SQLITE3_ASSOC))) {   var_dump($row);}?> `

Результат виконання цього прикладу:

array(1) {
["bar"]=>
string(3) "baz"
}
array(1) {
["bar"]=>
string(2) "42"
}

### Дивіться також

- [SQLite3Stmt::bindValue()](sqlite3stmt.bindvalue.md) - Зв'язує
значення параметра зі змінною підготовленого запиту
- [SQLite3::prepare()](sqlite3.prepare.md) - Підготовка
SQL-запит для виконання
