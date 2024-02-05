---
navigation:
  - pdo.sqlitecreatecollation.md: '« PDO::sqliteCreateCollation'
  - refs.database.vendors.md: Модулі для роботи з базами даних окремих виробників
  - index.md: PHP Manual
  - ref.pdo-sqlite.md: SQLite (PDO)
title: 'PDO::sqliteCreateFunction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::sqliteCreateFunction

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo\_sqlite >= 1.0.0)

PDO::sqliteCreateFunction — Реєстрація функції користувача для використання в SQL-запитах

### Опис

```methodsynopsis
public PDO::sqliteCreateFunction(    string $function_name,    callable $callback,    int $num_args = -1,    int $flags = 0): bool
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

Цей метод дозволяє вам реєструвати функцію PHP як функцію користувача SQLite (User Defined Function, UDF), що дозволить використовувати її в SQL-запитах.

UDF можна використовувати в будь-якому SQL-запиті, в якому дозволяється використовувати функції, наприклад, SELECT, UPDATE, а також у тригерах.

### Список параметрів

`function_name`

Ім'я функції для використання у запитах.

`callback`

Функція зворотного дзвінка для обробки дзвінків SQL-функції.

> **Зауваження**: Функція зворотного виклику повинна повертати значення зрозумілого типу SQLite (тобто [скалярного типу](language.types.intro.md)

Ця функція має бути визначена так:

```methodsynopsis
callback(mixed $value, mixed ...$values): mixed
```

`value`

Перший аргумент, що передається в SQL-функцію.

`values`

Подальші аргументи.

`num_args`

Кількість аргументів, які приймає функція. Якщо поставити рівним `-1`, то функція буде приймати будь-яку кількість аргументів.

`flags`

Побітова кон'юнкція (АБО) прапорів. На даний момент підтримується лише прапор \*\*`PDO::SQLITE_DETERMINISTIC`\*\*що визначає те, що функція завжди повертає однаковий результат для однакових вхідних значень.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.4 | Добавлен параметр`flags` |

### Приклади

**Пример #1 Пример использования**PDO::sqliteCreateFunction()\*\*\*\*

```php
<?php
function md5_and_reverse($string)
{
    return strrev(md5($string));
}

$db = new PDO('sqlite:sqlitedb');
$db->sqliteCreateFunction('md5rev', 'md5_and_reverse', 1);
$rows = $db->query('SELECT md5rev(filename) FROM files')->fetchAll();
?>
```

У цьому прикладі ми визначили функцію, що обчислює md5 суму рядка і перевертає її. Коли SQL-запит буде запущений, отримані значення filename будуть перетворені цією функцією. Результуючий набір `$rows` міститиме перетворені значення.

Краса такого підходу полягає в тому, що вам не потрібно після отримання результуючого набору пробігатися по ньому циклом. [foreach](control-structures.foreach.md) для обчислення необхідних значень.

**Підказка**

Ви можете використовувати [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md) і [PDO::sqliteCreateAggregate](pdo.sqlitecreateaggregate.md) для перевизначення стандартних функцій SQLite, що агрегують.

### Дивіться також

-   [PDO::sqliteCreateAggregate](pdo.sqlitecreateaggregate.md)
-   **sqlite\_create\_function()**
-   **sqlite\_create\_aggregate()**
