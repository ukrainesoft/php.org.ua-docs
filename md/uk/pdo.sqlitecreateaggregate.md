---
navigation:
  - ref.pdo-sqlite.connection.md: « PDOSQLITE DSN
  - pdo.sqlitecreatecollation.md: 'PDO::sqliteCreateCollation »'
  - index.md: PHP Manual
  - ref.pdo-sqlite.md: SQLite (PDO)
title: 'PDO::sqliteCreateAggregate'
---
# PDO::sqliteCreateAggregate

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdosqlite> = 1.0.0)

PDO::sqlite Create Aggregate — Реєстрація агрегуючої функції користувача для використання в SQL-запитах

### Опис

```methodsynopsis
public PDO::sqliteCreateAggregate(    string $function_name,    callable $step_func,    callable $finalize_func,    int $num_args = ?): bool
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

Цей метод аналогічний [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md), крім того, що він реєструє функцію, яку можна використовувати для обчислення агрегованого результату по всіх рядках у запиті.

Ключова відмінність цього методу від [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md) у тому, що для керування агрегуванням вимагає використання двох функцій.

### Список параметрів

`function_name`

Ім'я функції для використання у запитах.

`step_func`

Функція зворотного дзвінка для кожного рядка в результуючому наборі. Ваша PHP-функція повинна акумулювати результат та зберігати його у контексті агрегації.

Ця функція має бути визначена так:

```methodsynopsis
step(    mixed $context,    int $rownumber,    mixed $value,    mixed ...$values): mixed
```

`context`

Для першого рядка має дорівнювати **`null`**; Для всіх наступних рядків його значення має дорівнювати значенням, повернутим на попередньому кроці; Ви повинні використовувати його, щоб зберегти стан агрегації.

`rownumber`

Номер поточного рядка.

`value`

Перший аргумент передано агрегатору.

`values`

Подальші аргументи.

Значення функції, що повертається, буде використано як параметр `context` при наступному запуску функції, або як значення, що передається фіналізуючої функції.

`finalize_func`

Функція зворотного дзвінка для обчислення підсумкового значення агрегованого. Вона буде викликана як тільки всі рядки результуючого набору будуть оброблені, їй буде переданий контекст, що агрегує, і вона поверне фінальне значення. Ця функція має повернути значення типу зрозумілого SQLite (тобто . [скалярний тип](language.types.intro.md)

Ця функція має бути визначена так:

```methodsynopsis
fini(mixed $context, int $rowcount): mixed
```

`context`

Містить значення, повернене останнім викликом агрегуючої функції stepfunc.

`rowcount`

Кількість рядків, до яких застосовувалася функція, що агрегує.

Значення цієї функції, що повертається, буде використано як результат агрегації.

`num_args`

Підказка для парсера SQLite, якщо функція зворотного виклику отримує задану кількість аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад агрегуючої функції maxlength**

```php
<?php
$data = array(
   'one',
   'two',
   'three',
   'four',
   'five',
   'six',
   'seven',
   'eight',
   'nine',
   'ten',
   );
$db = new PDO('sqlite::memory:');
$db->exec("CREATE TABLE strings(a)");
$insert = $db->prepare('INSERT INTO strings VALUES (?)');
foreach ($data as $str) {
    $insert->execute(array($str));
}
$insert = null;

function max_len_step($context, $rownumber, $string)
{
    if (strlen($string) > $context) {
        $context = strlen($string);
    }
    return $context;
}

function max_len_finalize($context, $rowcount)
{
    return $context === null ? 0 : $context;
}

$db->sqliteCreateAggregate('max_len', 'max_len_step', 'max_len_finalize');

var_dump($db->query('SELECT max_len(a) from strings')->fetchAll());

?>
```

У цьому прикладі ми створили функцію, що агрегує, яка обчислює довжину найбільшого рядка в одному зі стовпців таблиці. Для кожного рядка викликається функція `max_len_step` і їй передається параметр `$context`. Цей параметр, як і будь-яка інша змінна PHP, може містити і масив, і об'єкт. У цьому прикладі вона використовується для зберігання максимальної довжини рядка; Якщо `$string` має довжину більшу, ніж міститься у контексті, ми оновлюємо контекст новим значенням.

Після обробки всіх рядків SQLite викличе функцію `max_len_finalize` для обчислення результату агрегації. У ній ми робимо обчислення, ґрунтуючись на даних з `$context`. У нашому простому прикладі ми просто повертаємо його значення, оскільки жодних додаткових обчислень не потрібно.

**Підказка**

Вкрай не рекомендується зберігати в контексті копії значень для обробки їх у фінальній функції, оскільки це спричинить велику перевитрату пам'яті SQLite для обробки запиту. Просто уявіть, скільки пам'яті вам знадобиться, якщо вам потрібно агрегувати, наприклад, мільйон значень по 32 байти.

**Підказка**

Ви можете використовувати [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md) і [PDO::sqliteCreateAggregate](pdo.sqlitecreateaggregate.md) для перевизначення стандартних функцій SQLite, що агрегують.

### Дивіться також

-   [PDO::sqliteCreateFunction](pdo.sqlitecreatefunction.md)
-   **sqlitecreatefunction()**
-   **sqlitecreateaggregate()**
