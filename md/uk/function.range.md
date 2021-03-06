- [«prev](function.prev.md)
- [reset »](function.reset.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Створює масив, що містить діапазон елементів

# range

(PHP 4, PHP 5, PHP 7, PHP 8)

range — Створює масив, що містить діапазон елементів

### Опис

**range**(string\|int\|float `$start`, string\|int\|float `$end`,
int\|float `$step` = 1): array

Створює масив, що містить діапазон елементів.

### Список параметрів

`start`
Перше значення послідовності.

`end`
Кінцеве значення, яким закінчується послідовність.

`step`
Якщо вказано параметр `step`, він буде використовуватися як інкремент
(або декремент) між елементами послідовності. Параметр `step` не
повинен дорівнювати `0` і не повинен виходити за межі зазначеного
діапазону. Якщо `step` не вказано, він набуває значення за замовчуванням 1.

### Значення, що повертаються

Повертає масив елементів від `start` до `end`, включно.

### Приклади

**Приклад #1 Приклади використання **range()****

` <?php// array(0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12)foreach (range(0, 12) as $number) { ;}echo "
";// Параметр step// array(0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100)foreach (range(0, 100, 10)   ;}echo "
";// Використання послідовності знаків// array('a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i');foreach ( range('a', 'i') as $letter) {   echo $letter;}echo "
";// array('c', 'b', 'a');foreach (range('c', 'a') as $letter) {   echo $letter;}?> `

### Примітки

> **Примітка**:
>
> Значення для послідовності знаків обмежені довжиною один
> символ. Якщо їх довжина більша за один, то тільки перший символ
> використовується.

### Дивіться також

- [shuffle()](function.shuffle.md) - Перемішує масив
- [array_fill()](function.array-fill.md) - Заповнює масив
значеннями
- [foreach](control-structures.foreach.md)
