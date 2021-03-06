- [«array_walk](function.array-walk.md)
- [arsort »](function.arsort.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- створює масив

# array

(PHP 4, PHP 5, PHP 7, PHP 8)

array - Створює масив

### Опис

**array**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$values`): array

Створює масив. Докладніше про масиви читайте у розділі
[Масиви](language.types.array.md).

### Список параметрів

`values`
Синтаксис "індекс = значення", розділені комами, визначає
індекси та їх значення. Індекс може бути рядком або цілим числом. Якщо
індекс опущений, буде автоматично згенерований числовий індекс, починаючи
з 0. Якщо індекс - число, наступним згенерованим індексом буде
число, що дорівнює максимальному числовому індексу + 1. Зверніть увагу,
що якщо визначено два однакові індекси, наступний перезапише
попередній.

Наявність завершальної коми після останнього елемента масиву, незважаючи
на деяку незвичайність є коректним синтаксисом.

### Значення, що повертаються

Повертає масив параметрів. Параметрам може бути призначений індекс з
допомогою оператора `=>`. Докладніше про масиви читайте у розділі
[Масиви](language.types.array.md).

### Приклади

Наступні приклади демонструють створення двомірного масиву,
визначення ключів асоціативних масивів та спосіб генерації числових
індексів для звичайних масивів, якщо нумерація починається з довільного
числа.

**Приклад #1 Приклад використання **array()****

`<?php$fruits = array (    "fruits"  => array("a" => "orange", "b" => "banana", "c" => "apple"),    (1, 2, 3, 4, 5, 6),   "holes"   => array("first", 5 => "second", "third"));?> `

**Приклад #2 Автоматична індексація за допомогою **array()****

` <?php$array = array(1, 1, 1, 1, 1, 8 => 1, 4 => 1, 19, 3 => 13);print_r($array);?> `

Результат виконання цього прикладу:

Array
(
[0] => 1
[1] => 1
[2] => 1
[3] => 13
[4] => 1
[8] => 1
[9] => 19
)

Зверніть увагу, що індекс '3' визначено двічі, і містить останній
значення 13. Індекс 4 визначено після індексу 8 і наступний
згенерований індекс (значення 19) - 9, починаючи з максимального
індексу 8.

Цей приклад створює масив, нумерація якого починається з першого.

**Приклад #3 Приклад використання **array()**, нумерація якого
починається з 1**

` <?php$firstquarter = array(1 => 'January', 'February', 'March');print_r($firstquarter);?> `

Результат виконання цього прикладу:

Array
(
[1] => January
[2] => February
[3] => March
)

Як і в Perl, ви маєте доступ до значень масиву всередині подвійних
лапок. Однак у PHP потрібно укласти ваш масив у фігурні дужки.

**Приклад #4 Доступ до масиву всередині подвійних лапок**

` <?php$foo = array('bar' => 'baz');echo "Hello {$foo['bar']}!"; // Hello baz!?> `

### Примітки

> **Примітка**:
>
> **array()** - мовна конструкція, що використовується для представлення
> літеральних масивів, а чи не проста функція.

### Дивіться також

- [array_pad()](function.array-pad.md) - Доповнити масив
певним значенням до вказаної довжини
- [list()](function.list.md) - Надає змінним зі списку
значення подібно до масиву
- [count()](function.count.md) - Підраховує кількість елементів
масиву або Countable об'єкті
- [range()](function.range.md) - Створює масив, що містить діапазон
елементів
- [foreach](control-structures.foreach.md)
- Тип [масив](language.types.array.md)
