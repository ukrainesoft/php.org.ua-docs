- [«switch](control-structures.switch.md)
- [declare »](control-structures.declare.md)

- [PHP Manual](index.md)
- [Керування конструкції](language.control-structures.md)
- match

## match

(PHP 8)

Вираз `match` призначений для розгалуження потоку виконання на
підставі перевірки збігу значення із заданою умовою. Аналогічно
оператору `switch`, вираз `match` приймає на вхід вираз,
яке порівнюється з безліччю альтернатив. Але, на відміну від
`switch`, воно обробляє значення у стилі, більше схожому на тернарний
оператор. Також, на відміну від `switch`, використовується суворе порівняння
(`===`), а не слабке (`==`). Вираз match доступний починаючи з PHP
8.0.0.

**Приклад #1 Структура вираження `match`**

` <?php$return_value = match (subject_expression) {    single_conditional_expression => return_expression,    conditional_expression1, conditional_expression2 => return;

**Приклад #2 Простий приклад використання `match`**

`<?php$food = 'cake';$return_value = match ($food) {   'apple' => 'На столі лежать яблуко',    'banana' =>'  На столі стоїть торт, var_dump ($ return_value);

Результат виконання цього прикладу:

string(35) "На столі стоїть торт"

> **Примітка**: Результат `match` використовувати не обов'язково.

> **Примітка**: Вираз `match` *має* завершуватися крапкою з комою
> `;`.

Вираз `match` схожий на оператор `switch` за винятком деяких
ключових відмінностей:

- На відміну від switch, `match` використовується суворе порівняння
(`===`).
- Вираз `match` повертає результат.
- В `match` виконується тільки одна, перша підійшла, гілка коду,
тоді як у `switch` відбувається наскрізне виконання починаючи з
підійшов умови і до першого оператора `break`, що зустрівся.
- Вираз `match` має бути вичерпним.

Також як і оператор `switch`, `match` послідовно проводить перевірки
на збіг із заданими умовами. Виконання коду умов відбувається
ліниво, тобто. код наступної умови виконується лише якщо всі
попередні перевірки провалилися. Буде виконана лише одна гілка коду,
відповідна умові, що підійшла. Приклад:

` <?php$result = match ($x) {    foo() => ...,   $this->bar() => ..., // $this->bar() не буде виконаний, () === $x    $this->baz => beep(), // beep() буде виконаний тільки якщо$x === $this->baz    // etc;

Умови в `match` можуть бути множинними. В цьому випадку їх слід
розділяти комами. Множинні умови працюють за принципом
логічного АБО і, по суті, є скороченою формою для випадків,
коли кілька умов мають оброблятися ідентично.

`<?php$result = match ($x) {    // Множинна умова:    $a, $b, $c => 5,    // Анологічно трем$                     => 5,};?> `

Також можна використати шаблон `default`. Цей шаблон збігається з чим
завгодно, навіщо не знайшлося збігів раніше. Наприклад:

` <?php$expressionResult = match ($condition) {    1, 2 => foo(),    3, 4 => bar(),    default => baz()

> **Примітка**: Використання декількох шаблонів default призведе до
> фатальної помилки **`E_FATAL_ERROR`**.

Вираз `match` має бути вичерпним. Якщо вираз, що перевіряється
не співпало з жодною з умов, то буде викинуто виняток
[UnhandledMatchError](class.unhandledmatcherror.md).

**Приклад #3 Приклад необробленого виразу**

` <?php$condition = 5;try {    match ($condition) {        1, 2 => foo(),        3, 4 => bar(),    };} catch (\UnhandledMatchError $e) {    var_dump($e );}?> `

Результат виконання цього прикладу:

object(UnhandledMatchError)#1 (7) {
["message":protected]=>
string(33) "Unhandled match value of type int"
["string":"Error":private]=>
string(0) ""
["code":protected]=>
int(0)
["file":protected]=>
string(9) "/in/ICgGK"
["line":protected]=>
int(6)
["trace":"Error":private]=>
array(0) {
}
["previous":"Error":private]=>
NULL
}

### Використання match для перевірки складних умов

Вираз `match` можна використовувати не лише для перевірки
ідентичності, але й для будь-яких виразів, що повертають логічне
значення. В цьому випадку як вхідний параметр передається
вираз `true`.

**Приклад #4 Використання match для розгалуження в залежності від входження
у діапазони цілих чисел**

` <?php$age = 23;$result = match (true) {    $age >= 65 => 'літній',   $age >= 25 => 'дорослий',                 default => 'дитина',};var_dump($result);?> `

Результат виконання цього прикладу:

string(11) "повнолітній"

**Приклад #5 Використання match для розгалуження залежно від
вмісту рядка**

` <?php$text = 'Bienvenue chez nous';$result = match (true) {   str_contains($text, 'Welcome') || str_contains($text, 'Hello') => 'en',    str_contains($text, 'Bienvenue') || str_contains($text, 'Bonjour') => 'fr',    // ...};var_dump($result);?> `

Результат виконання цього прикладу:

string(2) "fr"
