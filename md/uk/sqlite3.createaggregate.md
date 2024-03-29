---
navigation:
  - sqlite3.construct.md: '« SQLite3::\_\_construct'
  - sqlite3.createcollation.md: 'SQLite3::createCollation »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::createAggregate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SQLite3::createAggregate

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SQLite3::createAggregate — Зареєструвати функцію PHP як агрегуючу функцію SQL

### Опис

```methodsynopsis
public SQLite3::createAggregate(    string $name,    callable $stepCallback,    callable $finalCallback,    int $argCount = -1): bool
```

Реєструє функцію PHP або функцію користувача як агрегуючу функцію SQL для використання в запитах.

### Список параметрів

`name`

Ім'я агрегуючої функції SQL, яка має бути створена або перевизначена.

`stepCallback`

Функція зворотного дзвінка, яка буде викликана для кожного рядка результуючого набору. Ваша PHP-функція повинна акумулювати результат та зберігати його у контексті агрегації.

Ця функція має бути визначена так:

```methodsynopsis
step(    mixed $context,    int $rownumber,    mixed $value,    mixed ...$values): mixed
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

`finalCallback`

Функція зворотного дзвінка для обчислення підсумкового агрегованого значення. Вона буде викликана як тільки всі рядки результуючого набору будуть оброблені, їй буде переданий контекст, що агрегує, і вона поверне фінальне значення. Ця функція має повернути значення типу зрозумілого SQLite (тобто . [скалярний тип](language.types.intro.md)

Ця функція має бути визначена так:

```methodsynopsis
fini(mixed $context, int $rownumber): mixed
```

`context`

Містить результат останнього виклику функції, що агрегує.

`rownumber`

Завжди

Значення цієї функції буде використане як значення, що повертається всього агрегатора.

`argCount`

Кількість аргументів, які приймає функція агрегування SQL. Якщо значення є негативним, то функція може використовувати будь-яку кількість аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад агрегуючої функції max\_length**

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
$db = new SQLite3(':memory:');
$db->exec("CREATE TABLE strings(a)");
$insert = $db->prepare('INSERT INTO strings VALUES (?)');
foreach ($data as $str) {
    $insert->bindValue(1, $str);
    $insert->execute();
}
$insert = null;

function max_len_step($context, $rownumber, $string)
{
    if (strlen($string) > $context) {
        $context = strlen($string);
    }
    return $context;
}

function max_len_finalize($context, $rownumber)
{
    return $context === null ? 0 : $context;
}

$db->createAggregate('max_len', 'max_len_step', 'max_len_finalize');

var_dump($db->querySingle('SELECT max_len(a) from strings'));
?>
```

Результат виконання наведеного прикладу:

```
int(5)
```

У цьому прикладі ми написали функцію, що агрегує, яка обчислює найдовшого рядка в одній колонці таблиці. Для кожного рядка викликається функція `max_len_step` і їй передається параметр `$context`. Цей параметр нічим не відрізняється від звичайної змінної PHP і може спокійно містити масив або об'єкт. У цьому прикладі ми використовуємо її для збереження максимальної знайденої довжини рядка. Якщо `$string` буде мати довжину більше, ніж поточна збережена, значення контексту буде оновлено.

Після того, як усі рядки оброблені, SQLite викличе функцію `max_len_finalize`для остаточної підготовки результату. Тут ми можемо зробити необхідні розрахунки на основі даних з `$context`. У нашому простому прикладі ніяка постобробка не потрібна і ми просто повертаємо отримане значення.

**Підказка**

НЕ рекомендується зберігати копію значень у контексті, а обробку проводити у фінальній функції, оскільки це може призвести до великого споживання пам'яті під час обробки запиту. Просто уявіть, скільки пам'яті вам знадобиться для зберігання мільйона рядків, по 32 байти кожен, у пам'яті.

**Підказка**

Для перевизначення вбудованих в SQLite функцій, що агрегують, ви можете використовувати **SQLite3::createAggregate()**
