- [« ArrayObject::append](arrayobject.append.md)
- [ArrayObject::\_\_construct »](arrayobject.construct.md)

- [PHP Manual](index.md)
- [ArrayObject](class.arrayobject.md)
- Сортувати записи за значенням

# ArrayObject::asort

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

ArrayObject::asort — Сортування записів за значенням

### Опис

public **ArrayObject::asort**(int `$flags` = **`SORT_REGULAR`**): bool

Сортує елементи масиву в порядку зростання, тому його ключі
зберігають свою кореляцію зі значеннями, із якими пов'язані.

Використовується в основному для сортування асоціативних масивів, де важливий
фактичний порядок елементів.

> **Примітка**:
>
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій
> Початковий порядок. До PHP 8.0.0 їх відносний порядок
> відсортованому масиві був визначений.

### Список параметрів

`flags`
Необов'язковий другий параметр `flags` може використовуватись для
зміни поведінки сортування з використанням таких значень:

Прапори типу сортування:

- **`SORT_REGULAR`** - звичайне порівняння елементів; подробиці
описані в розділі [оператори порівняння](language.operators.comparison.md)
- **`SORT_NUMERIC`** - числове порівняння елементів
- **`SORT_STRING`** - рядкове порівняння елементів
- **`SORT_LOCALE_STRING`** - порівняння елементів як рядки на основі
поточний мовний стандарт. Використовується мовний стандарт,
який можна змінити за допомогою
[setlocale()](function.setlocale.md)
- **`SORT_NATURAL`** - порівняння елементів як рядки, використовуючи
"природний порядок", наприклад, [natsort()](function.natsort.md)
- **`SORT_FLAG_CASE`** - можна об'єднувати (побітове АБО) з
**`SORT_STRING`** або **`SORT_NATURAL`** для сортування рядків без
обліку регістру

### Значення, що повертаються

Функція завжди повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::asort()****

` <?php$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");$fruitArrayObject = new ArrayObject($fruits);$fruitArrayObject->asort();foreach ($fruitArrayObject as $key => $val) {    echo "$key = $val
";}?> `

Результат виконання цього прикладу:

c = apple
b = banana
d = lemon
a = orange

Назви фруктів були відсортовані в алфавітному порядку, та ключ,
пов'язаний із кожним записом, був збережений.

### Дивіться також

- [ArrayObject::ksort()](arrayobject.ksort.md) - Сортувати записи
за ключами
- [ArrayObject::natsort()](arrayobject.natsort.md) - Сортувати
масив, використовуючи алгоритм "natural order"
- [ArrayObject::natcasesort()](arrayobject.natcasesort.md) -
Сортувати масив, використовуючи реєстронезалежний алгоритм "natural
order"
- [ArrayObject::uasort()](arrayobject.uasort.md) - Сортувати
записи, використовуючи функцію користувача для порівняння елементів і
зберігаючи при цьому зв'язок ключ/значення
- [ArrayObject::uksort()](arrayobject.uksort.md) - Сортувати
масив за ключами, використовуючи користувальницьку функцію для порівняння
- [asort()](function.asort.md) - Сортує масив у порядку
зростання та підтримує асоціацію індексів
