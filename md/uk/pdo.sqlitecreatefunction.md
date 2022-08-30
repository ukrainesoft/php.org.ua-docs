Реєстрація функції користувача для використання в SQL-запитах

-   [« PDO::sqliteCreateCollation](pdo.sqlitecreatecollation.html)
    
-   [Модулі для роботи з базами даних окремих виробників](refs.database.vendors.html)
    
-   [PHP Manual](index.html)
    
-   [SQLite (PDO)](ref.pdo-sqlite.html)
    
-   Реєстрація функції користувача для використання в SQL-запитах
    

# PDO::sqliteCreateFunction

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdosqlite> = 1.0.0)

PDO::sqliteCreateFunction — Реєстрація функції користувача для використання в SQL-запитах

### Опис

```methodsynopsis
public PDO::sqliteCreateFunction(    string $function_name,    callable $callback,    int $num_args = -1,    int $flags = 0): bool
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

Цей метод дозволяє вам реєструвати функцію PHP як функцію користувача SQLite (User Defined Function, UDF), що дозволить використовувати її в SQL-запитах.

UDF можна використовувати у будь-якому SQL-запиті, у якому дозволяється використовувати функції, наприклад SELECT, UPDATE, і навіть у тригерах.

### Список параметрів

`function_name`

Ім'я функції для використання у запитах.

`callback`

Функція зворотного дзвінка для обробки дзвінків SQL-функції.

> **Зауваження**: Функція зворотного виклику повинна повертати значення зрозумілого типу SQLite (тобто [скалярного типа](language.types.intro.html)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `flags` |

### Приклади

**Приклад #1 Приклад використання **PDO::sqliteCreateFunction()****

```php
<?php
function md5_and_reverse($string)
{
    return strrev(md5($string));
}

$db = new PDO('sqlite:sqlitedb');
$db->sqliteCreateFunction('md5rev', 'md5_and_reverse', 1);
$rows = $db->query('SELECT md5rev(filename) FROM files')->fetchAll();
?>
```

У цьому прикладі ми визначили функцію, що обчислює md5 суму рядка і перевертає її. Коли SQL-запит буде запущено, отримані значення filename будуть перетворені цією функцією. Результуючий набір `$rows` міститиме перетворені значення.

Краса такого підходу полягає в тому, що вам не потрібно після отримання результуючого набору пробігатися по ньому циклом. [foreach](control-structures.foreach.html) для обчислення необхідних значень.

**Підказка**

Ви можете використовувати [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.html) і [PDO::sqliteCreateAggregate](pdo.sqlitecreateaggregate.html) для перевизначення стандартних функцій SQLite, що агрегують.

### Дивіться також

-   [PDO::sqliteCreateAggregate](pdo.sqlitecreateaggregate.html)
-   **sqlitecreatefunction()**
-   **sqlitecreateaggregate()**