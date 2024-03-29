---
navigation:
  - function.soundex.md: « soundex
  - function.sscanf.md: sscanf »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: sprintf
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sprintf

(PHP 4, PHP 5, PHP 7, PHP 8)

sprintf — Повертає відформатований рядок

### Опис

```methodsynopsis
sprintf(string $format, mixed ...$values): string
```

Возвращает строку, созданную с использованием строки формата`format`

### Список параметрів

`format`

Рядок формату складається з нуля або більше директив: звичайні символи (за винятком `%`), які просто виводяться без зміни та *специфікатори перетворення*, кожен із яких вимагає передачі свого параметра.

Специфікатори перетворення мають такий формат: `%[argnum$][flags][width][.precision]specifier`

##### Argnum

Ціло число, за яким слідує знак долара `$`, щоб вказати, який числовий аргумент обробляти під час перетворення.

**Прапори**

| Флаг | Опис |
| --- | --- |
| `-` | Вирівнювання по лівому краю в межах заданої ширини поля; За умовчанням вирівнювання відбувається праворуч. |
| `+` | Друкує плюс `+` у не негативних чисел; За замовчуванням знак друкується лише у негативних чисел. |
| (space) | Доповнює результат пробілами. Це стандартна поведінка. |
|  | Доповнює числа нулями (тільки зліва). Зі специфікатором `s` також може доповнювати нулями праворуч. |
| `'`(char) | Доповнює результат символом (char). |

##### Ширина

Або ціле число, що вказує, скільки символів (мінімум) має вийти в результаті перетворення, або `*`Если указано значение`*`ширина задається як додаткове ціле значення, що передує значенню, відформатованому специфікатором.

##### Точність

Крапка , з наступним цілим числом, або `*`значення якого залежить від специфікатора:

-   Для специфікаторів`e` `E` `f`и`F`: задає кількість цифр після десяткової коми (за замовчуванням 6).
-   Для специфікаторів`g`,`G` `h`и`H`: задає максимальне значення значущих цифр.
-   Для специфікатора`s`: визначає обмеження максимальної кількості символів у рядку, які будуть виведені.

> **Зауваження**: Якщо вказана точка без наступного значення точності, то точність буде вважатися 0. Якщо вказано значення `*`, точність задається як додаткове значення, що передує значенню, відформатованому специфікатором.

**Специфікатори**

| Спецификатор | Опис |
| --- | --- |
| `%` | Відсоток символ. Аргументи не потрібні. |
| `b` | Аргумент сприймається як ціле число і друкується у бінарному поданні. |
| `c` | Аргумент розглядається як ціле число і друкується як символ таблиці ASCII з відповідним кодом. |
| `d` | Аргумент сприймається як ціле число і друкується як ціле число зі знаком. |
| `e` | Аргумент вважається за число у науковій нотації (тобто 1.2e+2). |
| `E` | Аналогічно специфікатору `e`, але використовує великі символи (тобто 1.2E+2). |
| `f` | Аргумент вважається за число з точкою, що плаває (з урахуванням локалі). |
| `F` | Аргумент вважається за число з точкою, що плаває (без урахування локалі). |
| `g` |  |
| Загальний формат. |  |

Нехай P дорівнює точності, якщо вона не дорівнює нулю, 6 якщо точність не задана і 1, якщо точність задана як 0. Тоді, якщо перетворення зі стилем "E" матиме показник ступеня X:

Якщо P > X ≥ -4, перетворення буде в стилі "f" і точність буде P - (X + 1). У протилежному випадку перетворення буде в стилі "e" і точність буде P − 1.

`G` | Аналогічно специфікатору `g`, але використовує `E`и`f`. `h` | Аналогічно специфікатору `g`, але використовує `F`Доступен с PHP 8.0.0. | |`H` | Аналогічно специфікатору `g`, але використовує `E`и`F`Доступен с PHP 8.0.0. | |`o` | Аргумент сприймається як ціле число і друкується у вісімковому поданні. | | `s` | Аргумент розглядається та друкується як рядок. | | `u` | Аргумент сприймається як ціле число і друкується як беззнакове ціле число. | | `x` | Аргумент розглядається як ціле число і друкується у шістнадцятковому поданні (літери будуть у нижньому регістрі). | | `X` | Аргумент розглядається як ціле число і друкується у шістнадцятковому поданні (літери будуть у верхньому регістрі). |

**Увага**

Специфікатор `c` ігнорує значення ширини та доповнення

**Увага**

Спроба використовувати специфікатори із зазначенням ширини для рядка в багатобайтовому кодуванні може призвести до несподіваних результатів.

Змінні будуть приведені до відповідного для специфікатора типу:

**Обробка типів**

| Тип | Спецификатор |
| --- | --- |
| string | `s` |
| int | `d` `u` `c` `o` `x` `X` `b` |
| float | `e` `E` `f` `F` `g` `G` `h` `H` |

`values`

### Значення, що повертаються

Повертає рядок, відформатований відповідно до формату `format`

### Помилки

Починаючи з PHP 8.0.0, якщо кількість аргументів дорівнює нулю, викидається виняток [ValueError](class.valueerror.md). До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

Починаючи з PHP 8.0.0, якщо `[width]` менше нуля чи більше **`PHP_INT_MAX`**, викидається виняток [ValueError](class.valueerror.md). До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

Починаючи з PHP 8.0.0, якщо `[precision]` менше нуля чи більше **`PHP_INT_MAX`**, викидається виняток [ValueError](class.valueerror.md). До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

Починаючи з PHP 8.0.0, якщо аргументів встановлено менше, ніж потрібно, викидається виняток [ArgumentCountError](class.argumentcounterror.md). До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не повертає \*\*`false`\*\*в случае возникновения ошибки. |
| 8.0.0 | Викидає виняток [ValueError](class.valueerror.md)якщо кількість аргументів дорівнює нулю; раніше функція видавала помилку рівня **`E_WARNING`** |
| 8.0.0 | Викидає виняток [ValueError](class.valueerror.md), якщо `[width]` менше нуля чи більше **`PHP_INT_MAX`**; раніше функція видавала помилку рівня **`E_WARNING`** |
| 8.0.0 | Викидає виняток [ValueError](class.valueerror.md), якщо `[precision]` менше нуля чи більше **`PHP_INT_MAX`**; раніше функція видавала помилку рівня **`E_WARNING`** |
| 8.0.0 | Викидає виняток [ArgumentCountError](class.argumentcounterror.md)якщо аргументів задано менше, ніж потрібно; раніше функція видавала помилку рівня **`E_WARNING`** |

### Приклади

**Приклад #1 Argument swapping**

Рядок формату підтримує нумерацію та перемішування аргументів.

```php
<?php
$num = 5;
$location = 'tree';

$format = 'There are %d monkeys in the %s';
echo sprintf($format, $num, $location);
?>
```

Результат виконання наведеного прикладу:

```
There are 5 monkeys in the tree
```

Тепер уявімо, що рядок форматування задається у сторонньому файлі. Це звичайна практика за необхідності підтримки кількох мов. Уявімо, що рядок був переписаний таким чином:

```php
<?php
$format = 'The %s contains %d monkeys';
echo sprintf($format, $num, $location);
?>
```

Упс! У нас проблема – порядок специфікаторів перестав відповідати порядку аргументів. Так як нам дуже не хочеться змінювати код щоразу, коли змінюється формат рядка, то ми можемо використовувати нумеровані аргументи:

```php
<?php
$format = 'The %2$s contains %1$d monkeys';
echo sprintf($format, $num, $location);
?>
```

Додатковим приємним моментом є те, що ми можемо використовувати один параметр для кількох підстановок.

```php
<?php
$format = 'The %2$s contains %1$d monkeys.
           That\'s a nice %2$s full of %1$d monkeys.';
echo sprintf($format, $num, $location);
?>
```

При використанні нумерованих аргументів, *специфікатор позиції* `n$`должен стоять сразу же за символом процента (`%`), до будь-якого іншого специфікатора, як показано нижче.

**Приклад #2 Використання символу заповнення**

```php
<?php
echo sprintf("%'.9d\n", 123);
echo sprintf("%'.09d\n", 123);
?>
```

Результат виконання наведеного прикладу:

```
......123
000000123
```

**Приклад #3 Специфікатор позиції у комбінації з іншими специфікаторами**

```php
<?php
$format = 'The %2$s contains %1$04d monkeys';
echo sprintf($format, $num, $location);
?>
```

Результат виконання наведеного прикладу:

```
The tree contains 0005 monkeys
```

**Приклад #4**sprintf()**: ціле з лідируючими нулями**

```php
<?php
$isodate = sprintf("%04d-%02d-%02d", $year, $month, $day);
?>
```

**Приклад #5**sprintf()**: форматування грошових одиниць**

```php
<?php
$money1 = 68.75;
$money2 = 54.35;
$money = $money1 + $money2;
echo $money;
echo "\n";
$formatted = sprintf("%01.2f", $money);
echo $formatted;
?>
```

Результат виконання наведеного прикладу:

```
123.1
123.10
```

**Приклад #6**sprintf()**: наукова нотація**

```php
<?php
$number = 362525200;

echo sprintf("%.3e", $number);
?>
```

Результат виконання наведеного прикладу:

```
3.625e+8
```

### Дивіться також

-   [printf()](function.printf.md) \- Виводить відформатований рядок
-   [fprintf()](function.fprintf.md) \- Записує відформатований рядок у потік
-   [vprintf()](function.vprintf.md) \- Виводить відформатований рядок
-   [vsprintf()](function.vsprintf.md) \- Повертає відформатований рядок
-   [vfprintf()](function.vfprintf.md) \- Записує відформатований рядок у потік
-   [sscanf()](function.sscanf.md) \- Розбирає рядок відповідно до заданого формату
-   [fscanf()](function.fscanf.md) \- Обробляє дані з файлу відповідно до формату
-   [number\_format()](function.number-format.md) \- Форматує число з поділом груп
-   [date()](function.date.md) \- Форматує тимчасову мітку Unix
