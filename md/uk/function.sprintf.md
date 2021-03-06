- [«soundex](function.soundex.md)
- [sscanf»](function.sscanf.md)

- [PHP Manual](index.md)
- [Функції для роботи з рядками](ref.strings.md)
- Повертає відформатований рядок

# sprintf

(PHP 4, PHP 5, PHP 7, PHP 8)

sprintf — Повертає відформатований рядок

### Опис

**sprintf**(string `$format`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$values`): string

Повертає рядок, створений із використанням рядка формату `format`.

### Список параметрів

`format`
Рядок формату складається з нуля або більше директив: звичайні символи (за
винятком `%`), які просто виводяться без зміни та
*специфікатори перетворення*, кожен з яких вимагає передачі
свого параметра.

Специфікатори перетворення мають такий формат:
`%[argnum$][flags][width][.precision]specifier`.

##### Argnum

Ціле число, за яким слідує знак долара `$`, щоб вказати, який
числовий аргумент обробляти під час перетворення.

| Підкреслити | Опис                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------- |
| -           | Вирівнювання лівим краєм у межах заданої ширини поля; За умовчанням вирівнювання відбувається праворуч. |                                                                                                     
| +           | Друкує плюс + у не негативних чисел; За замовчуванням знак друкується лише у негативних чисел.          |
| (space)     | Доповнює результат пробілами. Це стандартна поведінка.                                                  | | | |                                                                                                        |                                                                                                     
| 0           | Доповнює числа нулями (тільки зліва). Зі специфікатором s також може доповнювати нулями праворуч.       |
| (char)      | Доповнює результат символом (char).                                                                     |

**Прапори**

##### Ширина

Ціле число, яке визначає мінімальну кількість символів, яка буде
надруковано.

##### Точність

Точка `.` з наступним цілим числом, що працює по-різному для різних
специфікаторів:

- Для специфікаторів `e`, `E`, `f` та `F`: задає кількість цифр
після десяткової коми (за замовчуванням 6).
- Для специфікаторів `g`, `G`, `h` та `H`: задає максимальне значення
друкованих значущих цифр.
- Для специфікатора `s`: визначає обмеження максимальної кількості
символів у рядку, які будуть виведені.

> **Примітка**: Якщо вказана точка без наступного значення точності,
> то точність буде рахуватися за 0.

> **Примітка**: Спроба використовувати специфікатор позиції зі значенням
> більше, ніж **`PHP_INT_MAX`** призведе до виведення попередження.

[TABLE]

**Специфікатори**

**Увага**
Специфікатор `c` ігнорує значення ширини та доповнення

**Увага**
Спроба використовувати специфікатори із зазначенням ширини для рядка в
багатобайтове кодування може призвести до несподіваних результатів.

Змінні будуть приведені до відповідного для специфікатора типу:

| Тип    | Специфікатор                           |
| ------ | -------------------------------------- |
| string | s                                      |
| int    | d, u, c, o, x, X, b                    |
| float  | 'e', 'E', 'f', 'F', 'g', 'G', 'h', 'H' |

**Обробка типів**

`values`

### Значення, що повертаються

Повертає рядок, відформатований відповідно до формату `format`.

### Список змін

| Версія | Опис                                                            |
| ------ | --------------------------------------------------------------- |
| 8.0.0  | Функція більше не повертає **false** у разі виникнення помилки. |

### Приклади

**Приклад #1 Argument swapping**

Рядок формату підтримує нумерацію та перемішування аргументів.

` <?php$num = 5;$location = 'tree';$format = 'There are %d monkeys in the %s';echo sprintf($format, $num, $location);?> `

Результат виконання цього прикладу:

There are 5 monkeys in the tree

Тепер уявімо, що рядок форматування задається у сторонньому файлі.
Це звичайна практика за необхідності підтримки кількох мов.
Уявімо, що рядок був переписаний таким чином:

` <?php$format = 'The %s contains %d monkeys';echo sprintf($format, $num, $location);?> `

Упс! У нас проблема – порядок специфікаторів перестав відповідати
порядок аргументів. Так як нам дуже не хочеться змінювати код щоразу,
коли змінюється формат рядка, ми можемо використовувати нумеровані
аргументи:

` <?php$format = 'The %2$s contains %1$d monkeys';echo sprintf($format, $num, $location);?> `

Додатковим приємним моментом є те, що ми можемо використати
один параметр для кількох підстановок.

` <?php$format = 'The %2$s contains %1$d monkeys. That's a nice %2$s full of %1$d monkeys.';echo sprintf($format, $num, $location);?> `

При використанні нумерованих аргументів *специфікатор позиції* `n$`
повинен стояти відразу ж за символом відсотка (`%`), до будь-якого іншого
специфікатора, як показано нижче.

**Приклад #2 Використання символу заповнення**

` <?phpecho sprintf("%'.9d
", 123);echo sprintf("%'.09d
", 123);?> `

Результат виконання цього прикладу:

......123
000000123

**Приклад #3 Специфікатор позиції у комбінації з іншими
специфікаторами**

` <?php$format = 'The %2$s contains %1$04d monkeys';echo sprintf($format, $num, $location);?> `

Результат виконання цього прикладу:

The tree contains 0005 monkeys

**Приклад #4 **sprintf()**: ціле з лідируючими нулями**

` <?php$isodate = sprintf("%04d-%02d-%02d", $year, $month, $day);?> `

**Приклад #5 **sprintf()**: форматування грошових одиниць**

` <?php$money1 = 68.75;$money2 = 54.35;$money = $money1 + $money2;echo $money;echo "
";$formatted = sprintf("%01.2f", $money);echo $formatted;?> `

Результат виконання цього прикладу:

123.1
123.10

**Приклад #6 **sprintf()**: наукова нотація**

` <?php$number = 362525200;echo sprintf("%.3e", $number);?> `

Результат виконання цього прикладу:

3.625e+8

### Дивіться також

- [printf()](function.printf.md) - Виводить відформатований рядок
- [fprintf()](function.fprintf.md) - Записує відформатовану
рядок у потік
- [vprintf()](function.vprintf.md) - Виводить відформатовану
рядок
- [vsprintf()](function.vsprintf.md) - Повертає відформатовану
рядок
- [vfprintf()](function.vfprintf.md) - Записує відформатовану
рядок у потік
- [sscanf()](function.sscanf.md) - Розбирає рядок відповідно до
заданим форматом
- [fscanf()](function.fscanf.md) - Обробляє дані з файлу в
відповідно до формату
- [number_format()](function.number-format.md) - Форматує число з
поділом груп
- [date()](function.date.md) - Форматує тимчасову мітку Unix
